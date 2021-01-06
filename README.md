# Jquery-Movie
![movie](https://user-images.githubusercontent.com/67215505/103747023-58571680-5045-11eb-8d92-5e0f3bac44c8.png)

## 삭제 기능

```
function deleteById(movieId) {
            // ajax요청 삭제 (delete, get BODY가 없다.)
            $.ajax({
                type: "delete",
                url: `http://113.198.238.82:8000/api/movie/${movieId}`,
                dataType: "text"
            })
                .done((result) => {
                    if (result === "ok") {
                        $(`#card-${movieId}`).remove(); // 데이터와 UI를 동기화
                        console.log(this);
                    } else {
                        alert("삭제가 실패하였습니다.");
                    }
                });
        }
```
