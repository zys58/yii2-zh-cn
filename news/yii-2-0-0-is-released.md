>[原文：http://www.yiiframework.com/news/](http://www.yiiframework.com/news/81/yii-2-0-0-is-released/)  
主翻译：@qiansen1386(东方孤思子) 校对： 时间：2014年10月13

Yii 2.0.0 终于发布了！
=================

经过三年多的密集开发，饱含了 [300 余位贡献者](https://github.com/yiisoft/yii2/graphs/contributors)的总计超过
[10,000 次提交](https://github.com/yiisoft/yii2/commits/master)的 Yii 2.0.0 终于来了！感谢各位的支持与耐心！

你们应该也都知道了，Yii 2.0 是前作 1.1 之后的完全重写。我们这么选择主要是为了构建出一个代表当下最先进水平的 PHP
框架，在保持 Yii 原本的简洁与可扩展性的基础上，又加入了最新的科技与最新的功能，从而使得它较之之前更胜一筹。今天我们非常荣幸地宣布，我们已经达到了我们的设计目标。
As you may have already known, Yii 2.0 is a complete rewrite over the
previous version 1.1. We made this choice in order to build a
state-of-the-art PHP framework by keeping the original simplicity and
extensibility of Yii while adopting the latest technologies and features
to make it even better. And today we are very glad to announce that we
have achieved our goal.

下面是一些关于 Yii 与 Yii 2.0 的链接：
Below are some useful links about Yii and Yii 2.0:

-   [Yii 项目官网](http://www.yiiframework.com)
-   [Yii 2.0 GitHub 项目仓库](https://github.com/yiisoft/yii2)：你可以 star（星标）、watch （关注）它来跟踪了解 Yii 开发的最新动态。
-   [Yii Facebook 小组](https://www.facebook.com/groups/yiitalk/)
-   [Yii Twitter 微博](https://twitter.com/yiiframework)
-   [Yii 领英（LinkedIn）小组](https://www.linkedin.com/groups/yii-framework-1483367)

在下面我们会总结一下这个大家期待已久的发布的一些闪光点。你若你实在迫不及待，也可以直接参考 [指南-入门篇](http://www.yiiframework.com/doc-2.0/guide-index.html#getting-started) 快速上手把玩。
In the following we will summarize some of the highlights of this long
awaited release. You may check out the [Getting
Started](http://www.yiiframework.com/doc-2.0/guide-index.html#getting-started)
section if you want to rush to try it out first.

闪光点
------
Highlights
----------

### 适应各项标准与最新科技
（Adopting Standards and Latest Technologies）

Yii 2.0 应用了 PHP 命名空间与 Trait（特质），[PSR
推荐开发标准](http://www.php-fig.org/psr/)，
[Composer 依赖管理工具](https://getcomposer.org/)，[Bower](http://bower.io/) 与
[NPM](https://www.npmjs.org/)前端依赖管理工具。所有这些改变都使得框架自身变得更清爽，与第三方类库之间更易协作。

Yii 2.0 adopts PHP namespaces and traits, [PSR
standards](http://www.php-fig.org/psr/),
[Composer](https://getcomposer.org/), [Bower](http://bower.io/) and
[NPM](https://www.npmjs.org/). All these make the framework more
refreshing and interoperable with other libraries.

### 可靠的基础类库
（Solid Foundation Classes）

跟 1.1 时代一样，Yii 2.0 支持用 getter 和
setter，[配置数组](http://www.yiiframework.com/doc-2.0/guide-concept-configurations.html)，
[事件（events）](http://www.yiiframework.com/doc-2.0/guide-concept-events.html)以及
[行为（behaviors）](http://www.yiiframework.com/doc-2.0/guide-concept-behaviors.html)来配置[对象属性（Object
Properties）](http://www.yiiframework.com/doc-2.0/guide-concept-properties.html)。新的实现更加高效，更具表现力。举例而言，你可以这样来响应事件：
Like in 1.1, Yii 2.0 supports [object
properties](http://www.yiiframework.com/doc-2.0/guide-concept-properties.html)
defined via getters and setters,
[configurations](http://www.yiiframework.com/doc-2.0/guide-concept-configurations.html),
[events](http://www.yiiframework.com/doc-2.0/guide-concept-events.html)
and
[behaviors](http://www.yiiframework.com/doc-2.0/guide-concept-behaviors.html).
The new implementation is more efficient and expressive. For example,
you can write the following code to respond to an event:

    $response = new yii\web\Response;
    $response->on('beforeSend', function ($event) {
        // 在此处响应 "beforeSend" 事件
    });

Yii 2.0 实现了[依赖注入容器](http://www.yiiframework.com/doc-2.0/guide-concept-di-container.html)和[服务定位器](http://www.yiiframework.com/doc-2.0/guide-concept-service-locator.html)。这些功能让使用 Yii 构建的应用更加容易定制与测试。
and [service
Yii 2.0 implements the [dependency injection
container](http://www.yiiframework.com/doc-2.0/guide-concept-di-container.html)
and [service
locator](http://www.yiiframework.com/doc-2.0/guide-concept-service-locator.html).
It makes the applications built with Yii more customizable and testable.

### 开发工具
（Development Tools）

Yii 2.0 包含了一系列的开发工具，让程序猿的人生不再那么苦逼。
Yii 2.0 comes with several development tools to make the life of
developers easier.

新的 [Yii debugger](http://www.yiiframework.com/doc-2.0/guide-tool-debugger.html)
允许你检视你应用内部的运行状况。它也可以用于性能调教，来找出影响应用性能的瓶颈所在。
The [Yii
debugger](http://www.yiiframework.com/doc-2.0/guide-tool-debugger.html)
allows you to examine the runtime internals of your application. It can
also be used to do performance profiling to find out the performance
bottlenecks in your application.

如 1.1，Yii 2.0 也提供 Gii，也就是[代码生成器](http://www.yiiframework.com/doc-2.0/guide-tool-gii.html)，它可以帮你省去开发中的一大块时间。Gii 非常易于扩展，允许你自定义或创建不一样的代码生成器。它还同时提供 Web 与命令行两种界面，以适应不同的用户偏好。
Like 1.1, Yii 2.0 also provides Gii, a [code generation
tool](http://www.yiiframework.com/doc-2.0/guide-tool-gii.html), that can
cut down a large portion of your development time. Gii is very
extensible, allowing you to customize or create different code
generators. Gii provides both Web and console interfaces to fit for
different user preferences.

Yii 1.1的 API 文档收到过很多的积极反馈。很多人反馈说他们也想为他们的应用提供类似的文档系统。Yii 2.0
实现了他们的愿望，带来了[文档生成器](https://github.com/yiisoft/yii2/tree/master/extensions/apidoc)扩展。该生成器支持
Markdown 语法，它可以让你以一种更为简单明了且富有充分表现力的时髦方式撰写文档。
The API documentation of Yii 1.1 has received a lot of positive
feedback. Many people expressed the wish to create a similar
documentation for their applications. Yii 2.0 realizes this with a
[documentation
generator](https://github.com/yiisoft/yii2/tree/master/extensions/apidoc).
The generator supports Markdown syntax which allows you to write
documentation in a more succinct and expressive fashion.

### 安全
（Security）

Yii 2.0 可以帮助你写出更加安全的代码。它包含内建的安全组件有效防止蛀牙（东方孤思子在搞什么鬼），SQL 注入，XSS 攻击，CSRF 攻击，Cookie 篡改，等等攻击。安全砖家 [汤姆·沃斯特（Tom 
Worster）](https://github.com/tom--)和[安东尼·法拉利（Anthony Ferrara）](https://github.com/ircmaxell)
帮我们并重写了部分安全相关的代码哦。
Yii 2.0 helps you to write more secure code. It has built-in support to
prevent SQL injections, XSS attacks, CSRF attacks, cookie tampering,
etc. Security experts [Tom Worster](https://github.com/tom--) and
[Anthony Ferrara](https://github.com/ircmaxell) even helped us review
and rewrite some of the security-related code.

### 数据库
（Databases）

带数据库从来没有这么容易过。Yii 2.0 支持 [DB
迁移](http://www.yiiframework.com/doc-2.0/guide-db-migrations.html)，[数据访问对象
(DAO)](http://www.yiiframework.com/doc-2.0/guide-db-dao.html)，[查询构造器（query
builder）](http://www.yiiframework.com/doc-2.0/guide-db-query-builder.html)
和 [活动记录（Active
Record）](http://www.yiiframework.com/doc-2.0/guide-db-active-record.html)。相较于 1.1，Yii 2.0 改进了 AR 的性能，并且通过 ActiveRecord（AR） 和 QueryBuilder(QB) 统一了查询数据的语法。下面的例子展现了你能如何用 AR 或 QB 方便地查询顾客（Customer）的数据。如你所见，两种方式均使用了跟 SQL 语法一脉相承的链式方法调用。
Working with databases has never been easier. Yii 2.0 supports [DB
migration](http://www.yiiframework.com/doc-2.0/guide-db-migrations.html),
[database access objects
(DAO)](http://www.yiiframework.com/doc-2.0/guide-db-dao.html), [query
builder](http://www.yiiframework.com/doc-2.0/guide-db-query-builder.html)
and [Active
Record](http://www.yiiframework.com/doc-2.0/guide-db-active-record.html).
Compared with 1.1, Yii 2.0 improves the performance of Active Record and
unifies the syntax for querying data via query builder and Active
Record. The following code shows how you can query customer data using
either query builder or Active Record. As you can see, both approaches
use chained method calls which are similar to SQL syntax.

    use yii\db\Query;
    use app\models\Customer;
     
    $customers = (new Query)->from('customer')
        ->where(['status' => Customer::STATUS_ACTIVE])
        ->orderBy('id')
        ->all();
     
    $customers = Customer::find()
        ->where(['status' => Customer::STATUS_ACTIVE])
        ->orderBy('id')
        ->asArray()
        ->all();

下面的代码展示了你如何用 AR 实现关系查询：
The following code shows how you can perform relational queries using
Active Record:

    namespace app\models;
     
    use app\models\Order;
    use yii\db\ActiveRecord;
     
    class Customer extends ActiveRecord
    {
        public static function tableName()
        {
            return 'customer';
        }
     
        // 定义和 Order 模型类之间的一对多关系
        public function getOrders()
        {
            return $this->hasMany(Order::className(), ['customer_id' => 'id']);
        }
    }
     
    // 返回 id 为 100 的客户
    $customer = Customer::findOne(100);
    // 返回该用户的所有过往订单
    $orders = $customer->orders;

还有下面的代码展示了如何更新一个客户记录。内部运行的时候，会用参数绑定来防止 SQL 注入攻击，并只向数据库中保存修改过的字段。
And the following code shows how you can update a Customer record.
Behind the scene, parameter binding is used to prevent SQL injection
attacks, and only modified columns are saved to DB.

    $customer = Customer::findOne(100);
    $customer->address = '123 Anderson St';
    $customer->save();  // 执行 SQL：UPDATE `customer` SET `address`='123 Anderson St' WHERE `id`=100

Yii 2.0 支持各种路子的数据库。除了传统的关系型数据库，Yii 2.0 还增加了对 Cubrid，ElasticSearch，Sphinx。它还支持 
NoSQL 的数据库，包括 Redis 和 MongoDB。更重要的是，所有的数据库使用同一套 Query Builder 和 ActiveRecord 的 
API，这使得你在多个数据库之间的切换变得小菜一碟了。而且，在使用 AR 的时候，你甚至可以关联不同数据库之间的数据（比如 
MySQL 和 Redis）。
Yii 2.0 supports the widest range of databases. Besides the traditional
relational databases, Yii 2.0 adds the support for Cubrid,
ElasticSearch, Sphinx. It also supports NoSQL databases, including Redis
and MongoDB. More importantly, the same query builder and Active Record
APIs can be used for all these databases, which makes it an easy task
for you to switch among different databases. And when using Active
Record, you can even relate data from different databases (e.g. between
MySQL and Redis).

对于拥有大型数据库和对高性能有一定要求的应用，Yii 
2.0 也提供了内建的[数据库复制与读写分离](http://www.yiiframework.com/doc-2.0/guide-db-dao.html#replication-and-read-write-splitting)支持。
For applications with big databases and high performance requirement,
Yii 2.0 also provides built-in support for [database replication and
read-write
splitting](http://www.yiiframework.com/doc-2.0/guide-db-dao.html#replication-and-read-write-splitting).

### RESTful APIs

仅需几行代码，Yii 2.0 让你快速构建一系列全功能，遵从最新协议的 [RESTful
APIs](http://www.yiiframework.com/doc-2.0/guide-rest-quick-start.html)。下面的例子展示了如何创建一个提供用户数据的
RESTful API 服务。

With a few lines of code, Yii 2.0 lets you to quickly build a set of
fully functional [RESTful
APIs](http://www.yiiframework.com/doc-2.0/guide-rest-quick-start.html)
that comply to the latest protocols. The following example shows how you
can create a RESTful API serving user data.

首先，创建一个控制器类 `app\controllers\UserController`，然后制定
`app\models\User` 为提供服务的模型：
First, create a controller class `app\controllers\UserController` and
specify `app\models\User` as the type of model being served:

    namespace app\controllers;
     
    use yii\rest\ActiveController;
     
    class UserController extends ActiveController
    {
        public $modelClass = 'app\models\User';
    }

之后，修改你应用配置中 `urlManager` 组件的配置数组，加入以 Pretty URL 的形式提供 user 数据的配置项：
Then, modify the configuration about the `urlManager` component in your
application configuration to serve user data in pretty URLs:

    'urlManager' => [
        'enablePrettyUrl' => true,
        'enableStrictParsing' => true,
        'showScriptName' => false,
        'rules' => [
            ['class' => 'yii\rest\UrlRule', 'controller' => 'user'],
        ],
    ]
    
这就是全部的要做的事！ 这个你刚刚创建的 API 支持：
That's all you need to do! The API you just created supports:

-   `GET /users`: （逐页）列出全部用户；
-   `HEAD /users`：显示 user 列表的概览信息；
-   `POST /users`：创建新用户；
-   `GET /users/123`：返回用户 123 的详细资料；
-   `HEAD /users/123`：显示 user 123 的概述；
-   `PATCH /users/123` 以及 `PUT /users/123`：更新 user 123;
-   `DELETE /users/123`：删除 user 123;
-   `OPTIONS /users`：显示对于 `/users` 端点所支持的动作；
-   `OPTIONS /users/123`: 显示对于 `/users/123` 端点所支持的动作。

你也可以像这样通过 `curl` 命令访问你的 API,
You may access your API with the `curl` command like the following,

    $ curl -i -H "Accept:application/json" "http://localhost/users"

    HTTP/1.1 200 OK
    Date: Sun, 02 Mar 2014 05:31:43 GMT
    Server: Apache/2.2.26 (Unix) DAV/2 PHP/5.4.20 mod_ssl/2.2.26 OpenSSL/0.9.8y
    X-Powered-By: PHP/5.4.20
    X-Pagination-Total-Count: 1000
    X-Pagination-Page-Count: 50
    X-Pagination-Current-Page: 1
    X-Pagination-Per-Page: 20
    Link: <http://localhost/users?page=1>; rel=self, 
          <http://localhost/users?page=2>; rel=next, 
          <http://localhost/users?page=50>; rel=last
    Transfer-Encoding: chunked
    Content-Type: application/json; charset=UTF-8

    [
        {
            "id": 1,
            ...
        },
        {
            "id": 2,
            ...
        },
        ...
    ]

### 缓存

和 1.1 一样，Yii 2.0 支持全系列的缓存选项，从服务器端的缓存，比如[片段缓存](http://www.yiiframework.com/doc-2.0/guide-caching-fragment.html)，
[查询缓存](http://www.yiiframework.com/doc-2.0/guide-caching-data.html#query-caching)，到客户端的 [HTTP
缓存](http://www.yiiframework.com/doc-2.0/guide-caching-http.html)。它们的支持基于多种缓存驱动，比如 APC，Memcache，文件缓存，数据库缓存，等等。

Like 1.1, Yii 2.0 supports a whole range of caching options, from server
side caching, such as [fragment
caching](http://www.yiiframework.com/doc-2.0/guide-caching-fragment.html),
[query
caching](http://www.yiiframework.com/doc-2.0/guide-caching-data.html#query-caching)
to client side [HTTP
caching](http://www.yiiframework.com/doc-2.0/guide-caching-http.html).
They are supported on a variety of caching drivers, including APC,
Memcache, files, databases, etc.

### 表单

在 1.1 中，你可以非常便捷地创建同时支持客户端与服务器端验证的 HTML 表单。在 
Yii 2.0 中，[操作表单](http://www.yiiframework.com/doc-2.0/guide-input-forms.html)
变得更加容易。下面的例子显示了你可以如何创建登陆界面。
In 1.1, you can quickly create HTML forms that support both client side
and server side validation. In Yii 2.0, it is even easier [working with
forms](http://www.yiiframework.com/doc-2.0/guide-input-forms.html). The
following example shows how you can create a login form.

首先撸一个 `LoginForm` 模型表示要收集的数据。在这个类中你要列举你要用来验证用户输入的规则。这些规则将来会用于自动生成所需客户端 JavaScript 验证逻辑。
First create a `LoginForm` model to represent the data being collected.
In this class, you will list the rules that should be used to validate
the user input. The validation rules will later be used to automatically
generate the needed client-side JavaScript validation logic.

    use yii\base\Model;
     
    class LoginForm extends Model
    {
        public $username;
        public $password;
     
        /**
         * @return array 验证规则
         */
        public function rules()
        {
            return [
                // 用户名和密码为必填项
                [['username', 'password'], 'required'],
                // 密码需要用 validatePassword() 验证
                ['password', 'validatePassword'],
            ];
        }
     
        /**
         * 验证密码
         * 该方法用于作为密码栏的行内验证器
         */
        public function validatePassword()
        {
            $user = User::findByUsername($this->username);
            if (!$user || !$user->validatePassword($this->password)) {
                $this->addError('password', '用户名或密码错误。');
            }
        }
    }

然后创建该登录表单的视图代码
Then create the view code for the login form:

    use yii\helpers\Html;
    use yii\widgets\ActiveForm;
     
    <?php $form = ActiveForm::begin() ?>
        <?= $form->field($model, 'username') ?>
        <?= $form->field($model, 'password')->passwordInput() ?>
        <?= Html::submitButton('Login') ?>
    <? ActiveForm::end() ?>

### 验证与授权
（Authentication and Authorization）

如 1.1 一样，Yii 2.0 提供了内建的用户验证与授权支持。它支持诸如登陆登出，基于 cookie 或 token 的[登录验证](http://www.yiiframework.com/doc-2.0/guide-security-authentication.html)，[访问控制过滤](http://www.yiiframework.com/doc-2.0/guide-security-authorization.html#access-control-filter)以及[基于角色的访问控制(RBAC)](http://www.yiiframework.com/doc-2.0/guide-security-authorization.html#role-based-access-control-rbac)。
Like 1.1, Yii 2.0 provides built-in support for user authentication and
authorization. It supports features such as login, logout, cookie-based
and token-based 
[authentication](http://www.yiiframework.com/doc-2.0/guide-security-authentication.html),
[access control
filter](http://www.yiiframework.com/doc-2.0/guide-security-authorization.html#access-control-filter)
and [role-based access control
(RBAC)](http://www.yiiframework.com/doc-2.0/guide-security-authorization.html#role-based-access-control-rbac).

Yii 2.0 也同样提供[通过外部凭证提供者进行验证](https://github.com/yiisoft/yii2-authclient)的能力。它支持 OpenID、OAuth1 和 OAuth2 等协议。
Yii 2.0 also provides the ability of the [authentication via external
credentials providers](https://github.com/yiisoft/yii2-authclient). It
supports OpenID, OAuth1 and OAuth2 protocols.

### 小部件（Widgets）

Yii 2.0 提供了包含丰富的 UI 元素的集合，称为[小部件（Widgets）](http://www.yiiframework.com/doc-2.0/guide-structure-widgets.html)，用以帮助我们快速构建可交互的用户界面。Yii 
2.0 已经内建了对于 [Bootstrap](http://getbootstrap.com/) 小部件和 [jQuery 
UI](http://jqueryui.com/) 小部件的原生支持。它也提供如分页，grid view（网格视图），list view（列表视图），Details（详情视图）等常用的小部件，它们一起让开发 Web 应用变成又速度，又享受的过程。举例来说的话，你可以用以下几行代码创建一个全功能战斗民族语言的 jQuery UI 日期选择器：
Yii 2.0 comes with a rich set of user interface elements, called
[widgets](http://www.yiiframework.com/doc-2.0/guide-structure-widgets.html),
to help you quickly build interactive user interfaces. It has built-in
support for [Bootstrap](http://getbootstrap.com/) widgets and [jQuery
UI](http://jqueryui.com/) widgets. It also provides commonly used
widgets such as pagers, grid view, list view, detail, all of which make
Web application development a truly speedy and enjoyable process. For
example, with the following lines of code, you can create a fully
functional jQuery UI date picker in Russian:

    use yii\jui\DatePicker;
     
    echo DatePicker::widget([
        'name' => 'date',
        'language' => 'ru',// ru 就是 Russian
        'dateFormat' => 'yyyy-MM-dd',
    ]);

### 助手类（Helpers）

Yii 2.0 提供了很多实用的[助手类](https://github.com/yiisoft/yii2/tree/master/framework/helpers)用来简化常见工作。比如，著名的
`Html` 助手就包含了一系列的静态方法用来创建不同种类的 HTML 标签。然后是，`Url` 助手类让你可以很容易地创建各种 URL，比如下面所示的那种： 
Yii 2.0 provides many useful [helper
classes](https://github.com/yiisoft/yii2/tree/master/framework/helpers)
to simplify some common tasks. For example, the `Html` helper includes a
set of methods to create different HTML tags, and the `Url` helper lets
you more easily creates various URLs, like shown below:

    use yii\helpers\Html;
    use yii\helpers\Url;
     
    // 创建一个包含很多国家的多选框列表
    echo Html::checkboxList('country', 'USA', $countries);
     
    // 生成一个类似于 "/index?r=site/index&src=ref1#name" 的 URL
    echo Url::to(['site/index', 'src' => 'ref1', '#' => 'name']);

### 国际化

Yii 包含对网站国际化的有力支持，也因此，它被广泛应用于世界各地。它支持[消息翻译](http://www.yiiframework.com/doc-2.0/guide-tutorial-i18n.html#message-translation)，以及 [视图翻译](http://www.yiiframework.com/doc-2.0/guide-tutorial-i18n.html#views)。它也支持基于地理位置的[单复数变化以及日期格式化](http://www.yiiframework.com/doc-2.0/guide-tutorial-i18n.html#advanced-placeholder-formatting)，并遵从 [ICU
标准](http://icu-project.org/apiref/icu4c/classMessageFormat.html)。举例，
Yii has strong support for internationalization, as it is being used all
over the world. It supports [message
translation](http://www.yiiframework.com/doc-2.0/guide-tutorial-i18n.html#message-translation)
as well as [view
translation](http://www.yiiframework.com/doc-2.0/guide-tutorial-i18n.html#views).
It also supports locale-based [plural forms and data
formatting](http://www.yiiframework.com/doc-2.0/guide-tutorial-i18n.html#advanced-placeholder-formatting),
which complies to the [ICU
standard](http://icu-project.org/apiref/icu4c/classMessageFormat.html).
For example,

    // 带有日期格式化的消息翻译
    echo \Yii::t('app', 'Today is {0, date}', time());
     
    // 带有复数形式的消息翻译
    echo \Yii::t('app', 'There {n, plural, =0{are no cats} =1{is one cat} other{are # cats}}!', ['n' => 0]);

### 模版引擎
（Template Engines）

Yii 2.0 使用 PHP 作为默认的模版语言。但同时也通过官方提供的[模版引擎扩展](http://www.yiiframework.com/doc-2.0/guide-tutorial-template-engines.html)支持了 [Twig](http://twig.sensiolabs.org/)
和 [Smarty](http://www.smarty.net/) 两种模版引擎。而且，你自己做支持其他模版引擎的扩展也是可以的。
Yii 2.0 uses PHP as its default template language. It also supports
[Twig](http://twig.sensiolabs.org/) and [Smarty](http://www.smarty.net/)
through its [template engine
extensions](http://www.yiiframework.com/doc-2.0/guide-tutorial-template-engines.html).
And it is also possible for you to create extensions to support other
template engines.

### 测试

Yii 2.0 通过集成 [Codeception 测试框架](http://codeception.com/)和 [Faker 数据拟真器](https://github.com/fzaninotto/Faker)进一步加强了对代码测试的支持力度。它同时包含有一个 Fixture （译者注：PHPunit 翻译为基境，工程领域一般称为测试夹具，用来提供一个模拟的测试数据环境）框架，它与 DB 迁移相绑定，允许你更灵活地管理你的模拟测试数据。
Yii 2.0 strengthens the testing support by integrating
[Codeception](http://codeception.com/) and
[Faker](https://github.com/fzaninotto/Faker). It also comes with a
fixture framework which coupled with DB migrations, allows you to manage
your fixture data more flexible.

### 应用模板

为了进一步帮你缩减开发时间，Yii 发布有两个应用程序模版，每一个都是一个全功能的互联网应用。[基础应用模版](http://www.yiiframework.com/doc-2.0/guide-start-installation.html#installing-via-composer)可以作为开发小型或简单网站的起点，比如公司门户，个人站点等等。而[高级应用模板](http://www.yiiframework.com/doc-2.0/guide-tutorial-advanced-app.html)则更适用于开发包含多个业务层，或由大型开发团体负责的大型企业应用。
To further cut down your development time, Yii is released with two
application templates, each being a fully functional Web application.
The [basic application
template](http://www.yiiframework.com/doc-2.0/guide-start-installation.html#installing-via-composer)
can be used as a starting point for developing small and simple Web
sites, such as company portals, personal sites. The [advanced
application
template](http://www.yiiframework.com/doc-2.0/guide-tutorial-advanced-app.html)
is more suitable for building large enterprise applications that involve
multiple tiers and a big developer team.

### 扩展（Extensions）

尽管 Yii 2.0 已经提供了很多屌炸天的功能，它的扩展结构使得它可以更屌更牛逼。Yii 
的扩展是指专门为 Yii 应用设计，提供即用功能的可再发行的软件包。很多 Yii 的内建功能也是通过（官方）扩展的形式提供的，比如 
[邮件扩展](http://www.yiiframework.com/doc-2.0/guide-tutorial-mailing.html) 和 
[Bootstrap 扩展](https://github.com/yiisoft/yii2-bootstrap)。Yii 一直也以庞大的用户贡献[扩展库](http://www.yiiframework.com/extensions/)而自豪，截止目前为止，该库有将近 1700 个扩展。我们同时也在 [packagist.org](https://packagist.org/search/?q=yii) 上发现有超过 1300 个 Yii 相关的包。
While Yii 2.0 already provides many powerful features, one thing that
makes Yii even more powerful is its extension architecture. Extensions
are redistributable software packages specifically designed to be used
in Yii applications and provide ready-to-use features. Many built-in
features of Yii are provided in terms of extensions, such as
[mailing](http://www.yiiframework.com/doc-2.0/guide-tutorial-mailing.html),
[Bootstrap](https://github.com/yiisoft/yii2-bootstrap). Yii also boasts
a big user-contributed [extension
library](http://www.yiiframework.com/extensions/) consisting of almost
1700 extensions, as the time of this writing. We also find there are
more than 1300 Yii-related packages on
[packagist.org](https://packagist.org/search/?q=yii).

上手入门
---------

要上手 Yii 2.0，可以简单地运行下面的命令：
To get started with Yii 2.0, simply run the following commands:

    # 在 Composer 全局安装 composer-asset-plugin 前端资源插件。（此步骤只需运行一次，一劳永逸）
    php composer.phar global require "fxp/composer-asset-plugin:1.0.0-beta3"

    # 安装基础应用模版
    php composer.phar create-project yiisoft/yii2-app-basic basic 2.0.0

上面的命令假定你已经安装有 [Composer](https://getcomposer.org/) 了。如果没有，请参考 [Composer 安装说明](http://getcomposer.org/doc/00-intro.md#installation-nix)安装一下。
The above commands assume you already have
[Composer](https://getcomposer.org/). If not, please follow the
[Composer installation
instructions](http://getcomposer.org/doc/00-intro.md#installation-nix)
to install it.

请注意在安装过程中可能会提示说要你输入你的 GitHub 用户名和密码。这是正常的，输入完继续就可以了。（译者注：貌似没有 GitHub 账号的孩子没法愉快的玩耍了）
Note that you may be prompted to enter your GitHub username and password
during the installation process. This is normal. Just enter them and
continue.

经过上面的指令之后，你就拥有了一个已经可以运行的 Web 应用。可以通过 `http://localhost/basic/web/index.php` 地址访问。
With the above commands, you have a ready-to-use Web application that
may be accessed through the URL `http://localhost/basic/web/index.php`.

升级（Upgrading）
---------

如果你是从之前 Yii 2.0 的开发预览版本升级（比如 2.0.0-beta，2.0.0-rc），请参考下面的[升级说明](https://github.com/yiisoft/yii2/blob/master/framework/UPGRADE.md)。
If you are upgrading from previous Yii 2.0 development releases (e.g.
2.0.0-beta, 2.0.0-rc), please follow the [upgrade
instructions](https://github.com/yiisoft/yii2/blob/master/framework/UPGRADE.md).

如果你是要从 Yii 1.1 升级上来，我们必须要先提醒你，这个过程可能并不简单，这主要是由于 Yii 2.0 是完全的重写，甚至相当多的语法都不一样。当然，绝大多数 Yii 1.1 的知识仍然适用于 2.0。请阅读[升级说明](http://www.yiiframework.com/doc-2.0/guide-intro-upgrade-from-v1.html)以了解 2.0 中引入了哪些主要的更改。
If you are upgrading from Yii 1.1, we have to warn you that it will not
be smooth, mainly because Yii 2.0 is a complete rewrite with many syntax
changes. However, most of your Yii knowledge still apply in 2.0. Please
read the [upgrade
instructions](http://www.yiiframework.com/doc-2.0/guide-intro-upgrade-from-v1.html)
to learn the major changes introduced in 2.0.

文档（Documentation）
-------------

Yii 2.0 提供 [权威指南（Definitive Guide，有时也被称为手册）](http://www.yiiframework.com/doc-2.0/guide-README.html) 以及 [类库参考（class reference，用于查询 API 和类库的功能和源码）](http://www.yiiframework.com/doc-2.0/index.html)。权威指南被翻译为[多种语言](https://github.com/yiisoft/yii2/tree/master/docs)。（译者注：包含了本仓库各位小伙伴贡献的简体中文版的成果哦。）
Yii 2.0 has a [definitive
guide](http://www.yiiframework.com/doc-2.0/guide-README.html) as well as
a [class reference](http://www.yiiframework.com/doc-2.0/index.html). The
definitive guide is also being translated into [many
languages](https://github.com/yiisoft/yii2/tree/master/docs).

这里还有一些与 Yii 2.0 相关的书籍[刚刚出版](https://www.packtpub.com/web-development/web-application-development-yii-2-and-php)或正在被知名大牛（如[Larry Ullman（拉瑞·厄尔曼）](http://www.larryullman.com/)）撰写。拉瑞兄还费时费力地帮我们润色了一些权威指南中的描述。还有 Alexander Makarow（亚历山大·马卡洛夫，GitHub名 samdark，来自战斗民族，核心团队中的二号人物）也在协调一本社区贡献的 [cookbook about Yii 2.0（Yii 2.0 菜谱）](https://github.com/samdark/yii2-cookbook)，他的前作 Yii 1.1 菜谱也广受好评。
There are also a few books about Yii 2.0 [just
published](https://www.packtpub.com/web-development/web-application-development-yii-2-and-php)
or being written by famous writers such as [Larry
Ullman](http://www.larryullman.com/). Larry even spends his time helping
us polish the definitive guide. And Alexander Makarov is coordinating a
community-contributed [cookbook about Yii
2.0](https://github.com/samdark/yii2-cookbook), following his
well-received cookbook about Yii 1.1.

鸣谢
-------

特此感谢[为 Yii 做过贡献的所有人](https://github.com/yiisoft/yii2/graphs/contributors)。你们的支持与贡献是无价的！
We hereby thank [everyone who has contributed to
Yii](https://github.com/yiisoft/yii2/graphs/contributors). Your support
and contributions are invaluable!