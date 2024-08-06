### 빨리 감기 병합
- 빨리 감기 병합은 두 브랜치가 부모-자식 관계일 때 사용된다.
- 즉, 한 브랜치에서 새로운 커밋이 발생하고, 다른 브랜치에서는 그 커밋을 덮어쓰지 않는 경우이다.
- 이런 경우, 두 브랜치를 병합할 때 Git은 단순히 더 높은 커밋을 가리키도록 브랜치를 이동시킨다. 이 과정에서 별도의 병합 커밋이 생성되지 않는다.


### 3방향 병합
- 3방향 병합은 두 브랜치가 부모-자식 관계가 아닌 경우에 사용된다.
- 두 브랜치가 동시에 변경 사항을 가지고 있을 때, Git은 공통의 조상 커밋을 찾아내고, 해당 조상 커밋으로부터 각 브랜치가 어떻게 변경되었는지를 비교하여 새로운 병합 커밋을 생성한다.


### 충돌
- Git에서 '충돌(conflict)'이란 두 가지 이상의 변경 사항이 서로 충돌할 때 발생한다.
- 이는 보통 두 개 이상의 브랜치에서 같은 파일의 같은 부분을 동시에 수정하고 병합하려 할 때 일어난다.
- Git는 어떤 변경 사항을 우선적으로 적용해야 할지 결정할 수 없기 때문에, 사용자에게 어떤 변경 사항을 적용할지 결정해야 하는 충돌 상황을 알린 후 충돌이 발생한 파일에 특별한 마커를 추가한다.
- 이 마커는 충돌이 발생한 위치와 각 브랜치에서의 변경 사항을 보여준다.


```js
document.addEventListener("DOMContentLoaded", function() {
    const input = document.querySelector("#todo-input");
    const addButton = document.querySelector("#add-button");
    const todoList = document.querySelector("#todo-list");

    addButton.addEventListener("click", function() {
        const todoText = input.value.trim();
        if (todoText !== "") {
            const listItem = document.createElement("li");
            listItem.textContent = todoText;

            const deleteButton = document.createElement("button");
            deleteButton.textContent = "Delete";
            deleteButton.addEventListener("click", function() {
                todoList.removeChild(listItem);
            });

            listItem.appendChild(deleteButton);
            todoList.appendChild(listItem);
            input.value = "";
        }
    });
});
```

