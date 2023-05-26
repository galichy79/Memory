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

Next, we'll move on to the second action.
Далее переходим ко второму действию.
Almost all web applications involve CRUD (Create, Read, Update, and Delete) operations.
Почти все веб-приложения включают операции CRUD (создание, чтение, обновление и удаление).
You may even find that the majority of the work your application does is CRUD. 
Вы даже можете обнаружить, что большая часть работы, которую выполняет ваше приложение, — это CRUD.
Rails acknowledges this, and provides many features to help simplify code doing CRUD.
Rails признает это и предоставляет множество функций, помогающих упростить код при выполнении CRUD.
Showing a Single Article
Отображение отдельной статьи
We currently have a view that lists all articles in our database. 
В настоящее время у нас есть представление, в котором перечислены все статьи в нашей базе данных.
Let's add a new view that shows the title and body of a single article.
Давайте добавим новое представление, которое показывает заголовок и основную часть одной статьи.
We start by adding a new route that maps to a new controller action (which we will add next).
Мы начинаем с добавления нового маршрута, который сопоставляется с новым действием контроллера (которое мы добавим позже).
This designates a route parameter. 
Это обозначает параметр маршрута.
A route parameter captures a segment of the request's path, and puts that value into the params Hash, which is accessible by the controller action.
Параметр маршрута захватывает сегмент пути запроса и помещает это значение в хэш params, доступный для действия контроллера.
Let's add that show action now, below the index action in app/controllers/articles_controller.rb:
Давайте добавим это действие show сейчас, под действием index в app/controllers/articles_controller.rb:
The show action calls Article.find (mentioned previously) with the ID captured by the route parameter. 
Действие show вызывает Article.find (упомянутый ранее) с идентификатором, захваченным параметром маршрута.
The returned article is stored in the @article instance variable, so it is accessible by the view. 
Возвращенная статья сохраняется в переменной экземпляра @article, поэтому она доступна для представления.
 By default, the show action will render app/views/articles/show.html.erb.
По умолчанию действие show будет отображать app/views/articles/show.html.erb.
Let's create app/views/articles/show.html.erb, with the following contents:
Давайте создадим app/views/articles/show.html.erb со следующим содержимым:
Now we can see the article when we visit http://localhost:3000/articles/1!
Теперь мы можем увидеть статью при посещении http://localhost:3000/articles/1!
To finish up, let's add a convenient way to get to an article's page.
Напоследок добавим удобный способ попасть на страницу статьи.
We'll link each article's title in app/views/articles/index.html.erb to its page:
Мы свяжем название каждой статьи в app/views/articles/index.html.erb с ее страницей:
7.2 Resourceful Routing
7.2 Ресурсная маршрутизация
So far, we've covered the "R" (Read) of CRUD.
До сих пор мы рассмотрели «R» (Чтение) CRUD.
We will eventually cover the "C" (Create), "U" (Update), and "D" (Delete).
В конечном итоге мы рассмотрим «C» (создать), «U» (обновить) и «D» (удалить).
As you might have guessed, we will do so by adding new routes, controller actions, and views. 
Как вы могли догадаться, мы сделаем это, добавив новые маршруты, действия контроллера и представления.
Whenever we have such a combination of routes, controller actions, and views that work together to perform CRUD operations on an entity, we call that entity a resource. 
Всякий раз, когда у нас есть такая комбинация маршрутов, действий контроллера и представлений, которые работают вместе для выполнения операций CRUD над объектом, мы называем этот объект ресурсом.
For example, in our application, we would say an article is a resource.
Например, в нашем приложении мы бы сказали, что статья является ресурсом.
Rails provides a routes method named resources that maps all of the conventional routes for a collection of resources, such as articles.
Rails предоставляет метод маршрутов с именем resources, который отображает все обычные маршруты для набора ресурсов, например статей.
So before we proceed to the "C", "U", and "D" sections, let's replace the two get routes in config/routes.rb with resources:
Итак, прежде чем мы перейдем к разделам «C», «U» и «D», давайте заменим два маршрута get в config/routes.rb на ресурсы:
The resources method also sets up URL and path helper methods that we can use to keep our code from depending on a specific route configuration.
Метод ресурсов также устанавливает вспомогательные методы URL и пути, которые мы можем использовать, чтобы наш код не зависел от конкретной конфигурации маршрута.
The values in the "Prefix" column above plus a suffix of _url or _path form the names of these helpers. 
Значения в столбце «Префикс» выше, а также суффикс _url или _path образуют имена этих помощников.
 For example, the article_path helper returns "/articles/#{article.id}" when given an article.
Например, помощник article_path возвращает «/articles/#{article.id}», когда получает статью.
We can use it to tidy up our links in app/views/articles/index.html.erb:
Мы можем использовать его, чтобы привести в порядок наши ссылки в app/views/articles/index.html.erb:
However, we will take this one step further by using the link_to helper. 
Однако мы сделаем еще один шаг вперед, используя помощник link_to.
The link_to helper renders a link with its first argument as the link's text and its second argument as the link's destination. 
Помощник link_to отображает ссылку с первым аргументом в виде текста ссылки и вторым аргументом в качестве пункта назначения ссылки.
If we pass a model object as the second argument, link_to will call the appropriate path helper to convert the object to a path. 
Если мы передаем объект модели в качестве второго аргумента, link_to вызовет соответствующий помощник пути для преобразования объекта в путь.
For example, if we pass an article, link_to will call article_path. 
Например, если мы передаем статью, link_to вызовет article_path.
7.3 Creating a New Article
7.3 Создание новой статьи
First, the user requests a form to fill out. 
Сначала пользователь запрашивает форму для заполнения.
Then, the user submits the form.
If there are no errors, then the resource is created and some kind of confirmation is displayed.
Если ошибок нет, то ресурс создается и выводится какое-то подтверждение.
Else, the form is redisplayed with error messages, and the process is repeated.
В противном случае форма повторно отображается с сообщениями об ошибках, и процесс повторяется.
In a Rails application, these steps are conventionally handled by a controller's new and create actions. 
В приложении Rails эти шаги обычно обрабатываются действиями new и create контроллера.
Let's add a typical implementation of these actions to app/controllers/articles_controller.rb, below the show action:
Давайте добавим типичную реализацию этих действий в app/controllers/articles_controller.rb под действием show:

The new action instantiates a new article, but does not save it.
Новое действие создает экземпляр новой статьи, но не сохраняет ее.
This article will be used in the view when building the form.
Эта статья будет использоваться в представлении при построении формы.
By default, the new action will render app/views/articles/new.html.erb, which we will create next.
По умолчанию новое действие будет отображать файл app/views/articles/new.html.erb, который мы создадим далее.

The create action instantiates a new article with values for the title and body, and attempts to save it.
Действие создания создает экземпляр новой статьи со значениями заголовка и основного текста и пытается сохранить ее.
If the article is saved successfully, the action redirects the browser to the article's page at "http://localhost:3000/articles/#{@article.id}". 
Если статья успешно сохранена, действие перенаправляет браузер на страницу статьи по адресу «http://localhost:3000/articles/#{@article.id}».
Else, the action redisplays the form by rendering app/views/articles/new.html.erb with status code 422 Unprocessable Entity. 
В противном случае действие повторно отображает форму, отображая app/views/articles/new.html.erb с кодом состояния 422 Unprocessable Entity.
The title and body here are dummy values.
Заголовок и тело здесь являются фиктивными значениями.
After we create the form, we will come back and change these.
После того, как мы создадим форму, мы вернемся и изменим их.
redirect_to will cause the browser to make a new request, whereas render renders the specified view for the current request. 
redirect_to заставит браузер сделать новый запрос, тогда как render отобразит указанное представление для текущего запроса.
It is important to use redirect_to after mutating the database or application state.
Важно использовать redirect_to после изменения состояния базы данных или приложения.
Otherwise, if the user refreshes the page, the browser will make the same request, and the mutation will be repeated.
В противном случае, если пользователь обновит страницу, браузер сделает тот же запрос, и мутация повторится.
7.3.1 Using a Form Builder
7.3.1 Использование конструктора форм
We will use a feature of Rails called a form builder to create our form.
Мы будем использовать функцию Rails, называемую построителем форм, для создания нашей формы.
Using a form builder, we can write a minimal amount of code to output a form that is fully configured and follows Rails conventions.
Используя построитель форм, мы можем написать минимальный объем кода для вывода формы, которая полностью настроена и соответствует соглашениям Rails.

Let's create app/views/articles/new.html.erb with the following contents:
Создадим app/views/articles/new.html.erb со следующим содержимым:
The form_with helper method instantiates a form builder. 
Вспомогательный метод form_with создает экземпляр конструктора форм.
In the form_with block we call methods like label and text_field on the form builder to output the appropriate form elements.
В блоке form_with мы вызываем такие методы, как label и text_field в построителе форм для вывода соответствующих элементов формы.
The resulting output from our form_with call will look like:
Результирующий вывод нашего вызова form_with будет выглядеть так:
7.3.2 Using Strong Parameters
7.3.2 Использование сильных параметров
Submitted form data is put into the params Hash, alongside captured route parameters. 
Отправленные данные формы помещаются в хэш params вместе с захваченными параметрами маршрута.
Thus, the create action can access the submitted title via params[:article][:title] and the submitted body via params[:article][:body]. 
Таким образом, действие создания может получить доступ к отправленному заголовку через params[:article][:title] и к отправленному телу через params[:article][:body].
We could pass these values individually to Article.new, but that would be verbose and possibly error-prone.
Мы могли бы передать эти значения по отдельности в Article.new, но это было бы многословно и, возможно, чревато ошибками.
And it would become worse as we add more fields.
И будет еще хуже, если мы добавим больше полей.
Instead, we will pass a single Hash that contains the values.
Вместо этого мы передадим один хэш, содержащий значения.
However, we must still specify what values are allowed in that Hash. 
Однако мы все равно должны указать, какие значения разрешены в этом хэше.
Otherwise, a malicious user could potentially submit extra form fields and overwrite private data.
В противном случае злоумышленник может отправить дополнительные поля формы и перезаписать личные данные.
In fact, if we pass the unfiltered params[:article] Hash directly to Article.new, Rails will raise a ForbiddenAttributesError to alert us about the problem.
На самом деле, если мы передадим нефильтрованный хэш params[:article] непосредственно в Article.new, Rails вызовет ForbiddenAttributesError, чтобы предупредить нас о проблеме.
So we will use a feature of Rails called Strong Parameters to filter params. Think of it as strong typing for params.
На самом деле, если мы передадим нефильтрованный хэш params[:article] непосредственно в Article.new, Rails вызовет ForbiddenAttributesError, чтобы предупредить нас о проблеме.
Let's add a private method to the bottom of app/controllers/articles_controller.rb named article_params that filters params. 
Давайте добавим частный метод в конец app/controllers/articles_controller.rb с именем article_params, который фильтрует параметры.
And let's change create to use it:
И давайте изменим create, чтобы использовать его:
7.3.3 Validations and Displaying Error Messages
7.3.3 Проверка и отображение сообщений об ошибках
The first validation declares that a title value must be present.
Первая проверка объявляет, что должно присутствовать значение title.
Because title is a string, this means that the title value must contain at least one non-whitespace character.
Поскольку заголовок — это строка, это означает, что значение заголовка должно содержать хотя бы один непробельный символ.
With our validations in place, let's modify app/views/articles/new.html.erb to display any error messages for title and body:
С нашими проверками давайте изменим app/views/articles/new.html.erb, чтобы отображались любые сообщения об ошибках для заголовка и тела:
The full_messages_for method returns an array of user-friendly error messages for a specified attribute. 
Метод full_messages_for возвращает массив удобных для пользователя сообщений об ошибках для указанного атрибута.
 If there are no errors for that attribute, the array will be empty.
Если для этого атрибута нет ошибок, массив будет пустым.
7.3.4 Finishing Up
7.3.4 Завершение
We can now create an article by visiting http://localhost:3000/articles/new. 
To finish up, let's link to that page from the bottom of app/views/articles/index.html.erb:
Чтобы закончить, давайте добавим ссылку на эту страницу в нижней части app/views/articles/index.html.erb:
7.4 Updating an Article
7.4 Обновление статьи
These steps are conventionally handled by a controller's edit and update actions.
Эти шаги обычно обрабатываются действиями редактирования и обновления контроллера.
Let's add a typical implementation of these actions to app/controllers/articles_controller.rb, below the create action:
Давайте добавим типичную реализацию этих действий в app/controllers/articles_controller.rb под действием создания:
Notice how the edit and update actions resemble the new and create actions.
Обратите внимание, как действия редактирования и обновления напоминают действия создания и создания.

The edit action fetches the article from the database, and stores it in @article so that it can be used when building the form. 
Действие редактирования извлекает статью из базы данных и сохраняет ее в @article, чтобы ее можно было использовать при построении формы.
By default, the edit action will render app/views/articles/edit.html.erb.
По умолчанию действие редактирования отобразит app/views/articles/edit.html.erb.
The update action (re-)fetches the article from the database, and attempts to update it with the submitted form data filtered by article_params. 
Действие обновления (повторно) извлекает статью из базы данных и пытается обновить ее с помощью отправленных данных формы, отфильтрованных с помощью article_params.
If no validations fail and the update is successful, the action redirects the browser to the article's page. 
Если никакие проверки не завершаются неудачно и обновление выполнено успешно, действие перенаправляет браузер на страницу статьи.
Else, the action redisplays the form — with error messages — by rendering app/views/articles/edit.html.erb.
В противном случае действие повторно отображает форму — с сообщениями об ошибках — путем рендеринга app/views/articles/edit.html.erb.
7.4.1 Using Partials to Share View Code
7.4.1 Использование Partials для совместного использования кода просмотра
Our edit form will look the same as our new form. 
Наша форма редактирования будет выглядеть так же, как наша новая форма.
Even the code will be the same, thanks to the Rails form builder and resourceful routing. 
Даже код будет таким же благодаря конструктору форм Rails и находчивой маршрутизации.
The form builder automatically configures the form to make the appropriate kind of request, based on whether the model object has been previously saved.
Конструктор форм автоматически настраивает форму для выполнения запроса соответствующего типа в зависимости от того, был ли ранее сохранен объект модели.
Because the code will be the same, we're going to factor it out into a shared view called a partial. 
Поскольку код будет таким же, мы собираемся выделить его в общее представление, называемое частичным.
Let's create app/views/articles/_form.html.erb with the following contents:
Создадим app/views/articles/_form.html.erb со следующим содержимым:
The above code is the same as our form in app/views/articles/new.html.erb, except that all occurrences of @article have been replaced with article.
Приведенный выше код аналогичен нашей форме в app/views/articles/new.html.erb, за исключением того, что все вхождения @article заменены на article.
Because partials are shared code, it is best practice that they do not depend on specific instance variables set by a controller action.
Поскольку частичные фрагменты являются общим кодом, рекомендуется, чтобы они не зависели от конкретных переменных экземпляра, установленных действием контроллера.
Instead, we will pass the article to the partial as a local variable.
Вместо этого мы передадим статью в партиал как локальную переменную.
Let's update app/views/articles/new.html.erb to use the partial via render:
Давайте обновим app/views/articles/new.html.erb, чтобы использовать партиал через рендеринг:
A partial's filename must be prefixed with an underscore, e.g. _form.html.erb. But when rendering, it is referenced without the underscore, e.g. render "form".
Имя частичного файла должно начинаться с символа подчеркивания, например. _form.html.erb. Но при рендеринге на него ссылаются без подчеркивания, например. сделать "форму".
And now, let's create a very similar app/views/articles/edit.html.erb:
А теперь давайте создадим очень похожее приложение/views/articles/edit.html.erb:
7.4.2 Finishing Up
7.4.2 Завершение
We can now update an article by visiting its edit page, e.g. http://localhost:3000/articles/1/edit.
Теперь мы можем обновить статью, посетив ее страницу редактирования, например. http://localhost:3000/articles/1/edit.
To finish up, let's link to the edit page from the bottom of app/views/articles/show.html.erb:
7.5 Deleting an Article
Finally, we arrive at the "D" (Delete) of CRUD. 
Наконец, мы приходим к «D» (Удалить) CRUD.
Deleting a resource is a simpler process than creating or updating. It only requires a route and a controller action. 
Удаление ресурса — более простой процесс, чем создание или обновление. Для этого требуется только маршрут и действие контроллера.
And our resourceful routing (resources :articles) already provides the route, which maps DELETE /articles/:id requests to the destroy action of ArticlesController.
И наша находчивая маршрутизация (resources :articles) уже обеспечивает маршрут, который сопоставляет запросы DELETE /articles/:id с действием уничтожения ArticlesController.
So, let's add a typical destroy action to app/controllers/articles_controller.rb, below the update action:
Итак, давайте добавим типичное действие уничтожения в app/controllers/articles_controller.rb под действием обновления:
The destroy action fetches the article from the database, and calls destroy on it. Then, it redirects the browser to the root path with status code 303 See Other.
Действие уничтожения извлекает статью из базы данных и вызывает для нее уничтожение. Затем он перенаправляет браузер на корневой путь с кодом состояния 303 See Other.
We have chosen to redirect to the root path because that is our main access point for articles.
Мы решили перенаправить на корневой путь, потому что это наша основная точка доступа к статьям.
But, in other circumstances, you might choose to redirect to e.g. articles_path.
Но в других обстоятельствах вы можете перенаправить, например, на статьи_путь.
Now let's add a link at the bottom of app/views/articles/show.html.erb so that we can delete an article from its own page:
Теперь добавим ссылку внизу app/views/articles/show.html.erb, чтобы мы могли удалить статью с ее собственной страницы:
In the above code, we use the data option to set the data-turbo-method and data-turbo-confirm HTML attributes of the "Destroy" link.
В приведенном выше коде мы используем параметр данных для установки HTML-атрибутов data-turbo-method и data-turbo-confirm ссылки «Уничтожить».
 Both of these attributes hook into Turbo, which is included by default in fresh Rails applications.
Оба этих атрибута подключаются к Turbo, который по умолчанию включен в новые приложения Rails.
