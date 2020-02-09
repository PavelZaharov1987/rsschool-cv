# Резюме #

1. My name is Pavel Zakharov.

2. You can contact with me for:
    - mail: pavelzakharov@gmail.com;
    - phone: 8-905-274-7285.
    
3. I'm the Junior Developer. And my goal ability to learn fast and to be always in trend. 
I don’t expect everyone to teach me and find a way to find new things from everywhere.

4. My skills:
    - HTML5, CSS3;
    - JS, jquery;
    - GIT;
    - pug, less, sass;
    - webpack 4.

5. Implemented form cloning on the site as a function of adding details. Code examples:
    
    - HTML
    
    ```html
    <div class="orders">
        <form action="assets/php/send_order.php" method="POST" enctype="multipart/form-data">
            <ul>
                <li class="form-input"> 
                    <svg width="17" height="25">
                        <path stroke="#fff" stroke-width="1" fill="none" d="M 0,0 17,8 17,16 0,25"></path>
                    </svg>
                    <input type="text" name="title" placeholder="Название заказа" required>
                </li>
            </ul>
            <ul class="form-group">
                <li class="form-input"> 
                    <p>Деталь №1</p>
                </li>
                <li class="form-input">
                    <svg width="17" height="25">
                        <path stroke="#fff" stroke-width="1" fill="none" d="M 0,0 17,8 17,16 0,25"></path>
                    </svg>
                    <input type="text" placeholder="название детали" name="name-1" id="name" required>
                </li>
                <li class="form-input">
                    <svg width="17" height="25">
                        <path stroke="#fff" stroke-width="1" fill="none" d="M 0,0 17,8 17,16 0,25"></path>
                    </svg>
                    <input type="text" placeholder="количество деталей" oninput="this.value = this.value.replace(/[^0-9.]/g, ''); this.value = this.value.replace(/(\..*)\./g, '$1');" name="count-1" id="count" required>
                </li>
                <li class="form-input">
                    <svg width="17" height="25">
                        <path stroke="#fff" stroke-width="1" fill="none" d="M 0,0 17,8 17,16 0,25"></path>
                    </svg>
                    <textarea name="comment-1" cols="100" rows="3" placeholder="добавьте комментарий" id="comment"></textarea>
                </li>
                <li class="form-input">
                    <svg width="17" height="25">
                        <path stroke="#fff" stroke-width="1" fill="none" d="M 0,0 17,8 17,16 0,25"></path>
                    </svg>
                    <div class="add-file">
                        <label class="file-name" for="file-1">добавить архив чертежей или 3d моделей</label>
                        <input class="inputfile inputfile-1" type="file" name="file-1[]" id="file-1" data-multiple-caption="{count} files selected" multiple>
                    </div>
                </li>
                <li class="form-input">
                    <div class="add-button">
                        <button class="deleteProduct">удалить деталь</button>
                        <button class="addProduct">добавить деталь </button>
                        <input type="submit" value="оформить заказ" id="submit-order">
                    </div>
                </li>
            </ul>
        </form>
    </div>
    ```
    
    - JS (jquery)

    ```javascrypt
    $('.addProduct').click(function(e) {
        e.preventDefault();
        $('.deleteProduct').show();
        count++;
        var
          formGroup = $(this).closest('.form-group'),
          product = formGroup.clone(true, true);
        formGroup.after(product);
        $('.form-group:last-child input[type="text"], .form-group:last-child textarea').val('');
        $('.form-group:last-child .file-name').text('добавить архив чертежей или 3d моделей');
        $('.form-group:last-child .form-input:first-child p').text('Деталь №' + count);
        $('.form-group:last-child .add-file input').attr({
          'name': 'file-' + count + '[]',
          'id': 'file-' + count,
          'class': 'inputfile inputfile-' + count
        });
        $('.form-group:last-child #name').attr('name', 'name-' + count);
        $('.form-group:last-child #count').attr('name', 'count-' + count);
        $('.form-group:last-child #comment').attr('name', 'comment-' + count);
        $('.form-group:last-child #cost').attr('name', 'cost-' + count);
        $('.form-group:last-child .add-file label').attr('for', 'file-' + count);
      })
      $('.deleteProduct').click(function () {
        n++;
        $(this).closest('.form-group').detach();
        $('.form-group:last-child .addProduct, .form-group:last-child input[type="submit"]').show();
        if (count - n === 0)
          $('.deleteProduct').hide();
      });
      ```
  
  6. Experience:
      - [my latest project](https://customthings.ru);
      - i’ll add other projects after learning RSSchool.
      
  7. Education:
      - RSSchool;
      - GLO Academy;
      - HTMLAcademy;
      - w3schools.com.
      
  8. My english level - Elementary.  
  I'm improve my English with servise "Rosetta Stone" and watch TV shows and movies in English.
      
