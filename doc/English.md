permission denied - в правах отказано

You unlocked new Achievements with private contributions! Show them off by including private contributions in your Profile in settings.

Вы разблокировали новые достижения с частными вкладами! Покажите их, включив личные взносы в ваш профиль в настройках.

Introduction - вступление.

Access Denied - Доступ запрещен.

pick the donut - пик зе донат - выбрать пончик

contributors - участники

enhanced - повышенный

appropriate controller and action.
соответствующий контроллер и действие.
following root route to the top of the 
следующий корневой маршрут к вершине
Rails applications do not use require to load application code.
Приложения Rails не требуют загрузки кода приложения.
So far
До сих пор
The call to create_table specifies how the articles table should be constructed.
Вызов create_table указывает, как должна быть построена таблица статей.
and so on.
и так далее.
Inside the block for create_table, two columns are defined: title and body. 
Внутри блока для create_table определены два столбца: title и body.
As we will see, Rails will manage these for us, setting the values when we create or update a model object.
Как мы увидим, Rails будет управлять ими за нас, устанавливая значения при создании или обновлении объекта модели.
Let's run our migration with the following command:
Давайте запустим нашу миграцию с помощью следующей команды:
Now we can interact with the table using our model.
Теперь мы можем взаимодействовать с таблицей, используя нашу модель.
Using a Model to Interact with the Database
Использование модели для взаимодействия с базой данных
At this prompt, we can initialize a new Article object:
В этом приглашении мы можем инициализировать новый объект статьи:
It's important to note that we have only initialized this object. 
Важно отметить, что мы только инициализировали этот объект.
This object is not saved to the database at all.
Пока это доступно только в консоли.
It's only available in the console at the moment.
Этот объект вообще не сохраняется в базе данных.
To save the object to the database, we must call save:
Чтобы сохранить объект в базу данных, мы должны вызвать save:
The above output shows an INSERT INTO "articles" ... database query. 
В приведенном выше выводе показан запрос базы данных INSERT INTO «articles»...
The id, created_at, and updated_at attributes of the object are now set. 
Атрибуты id, created_at и updated_at объекта теперь установлены.
When we want to fetch this article from the database, we can call find on the model and pass the id as an argument:
Когда мы хотим получить эту статью из базы данных, мы можем вызвать find для модели и передать идентификатор в качестве аргумента:
This method returns an ActiveRecord::Relation object, which you can think of as a super-powered array.
Этот метод возвращает объект ActiveRecord::Relation, который можно рассматривать как сверхмощный массив.
Showing a List of Articles
Отображение списка статей
Controller instance variables can be accessed by the view. 
Доступ к переменным экземпляра контроллера может быть получен из представления.
That means we can reference @articles in app/views/articles/index.html.erb.
Это означает, что мы можем ссылаться на @articles в app/views/articles/index.html.erb.
mixture - миксчеr
смесь
The <% %> tag means "evaluate the enclosed Ruby code."
Тег <% %> означает «выполнить прилагаемый код Ruby».