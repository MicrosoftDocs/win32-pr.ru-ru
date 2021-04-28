---
<span data-ttu-id="1e987-101">Title: WinMain описание точки входа приложения: WinMain: точка входа приложения MS. AssetID: 389da5d4-d0f9-4339-be6c-0f4fecc59316 MS. Topic: статья MS. Date: 05/31/2018</span><span class="sxs-lookup"><span data-stu-id="1e987-101">title: WinMain The Application Entry Point description: WinMain: The Application Entry Point ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316 ms.topic: article ms.date: 05/31/2018</span></span>
---

# <a name="winmain-the-application-entry-point"></a><span data-ttu-id="1e987-102">WinMain: точка входа приложения</span><span class="sxs-lookup"><span data-stu-id="1e987-102">WinMain: The Application Entry Point</span></span>

<span data-ttu-id="1e987-103">Каждая программа Windows включает функцию точки входа, которая называется **WinMain** или **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="1e987-103">Every Windows program includes an entry-point function that is named either **WinMain** or **wWinMain**.</span></span> <span data-ttu-id="1e987-104">Ниже приведена сигнатура для **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="1e987-104">Here is the signature for **wWinMain**.</span></span>


```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow);
```



<span data-ttu-id="1e987-105">Четыре параметра:</span><span class="sxs-lookup"><span data-stu-id="1e987-105">The four parameters are:</span></span>

-   <span data-ttu-id="1e987-106">*HINSTANCE* называется «обработчиком» экземпляра или «обработчиком» для модуля.</span><span class="sxs-lookup"><span data-stu-id="1e987-106">*hInstance* is something called a "handle to an instance" or "handle to a module."</span></span> <span data-ttu-id="1e987-107">Операционная система использует это значение для задания исполняемого файла (EXE) при его загрузке в память.</span><span class="sxs-lookup"><span data-stu-id="1e987-107">The operating system uses this value to identify the executable (EXE) when it is loaded in memory.</span></span> <span data-ttu-id="1e987-108">Этот экземпляр необходим для определенных функций Windows, например для загрузки значков или точечных рисунков.</span><span class="sxs-lookup"><span data-stu-id="1e987-108">The instance handle is needed for certain Windows functions—for example, to load icons or bitmaps.</span></span>
-   <span data-ttu-id="1e987-109">*хпревинстанце* не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="1e987-109">*hPrevInstance* has no meaning.</span></span> <span data-ttu-id="1e987-110">Он использовался в 16-разрядной версии Windows, но теперь всегда равен нулю.</span><span class="sxs-lookup"><span data-stu-id="1e987-110">It was used in 16-bit Windows, but is now always zero.</span></span>
-   <span data-ttu-id="1e987-111">*пкмдлине* содержит аргументы командной строки в виде строки Юникода.</span><span class="sxs-lookup"><span data-stu-id="1e987-111">*pCmdLine* contains the command-line arguments as a Unicode string.</span></span>
-   <span data-ttu-id="1e987-112">*нкмдшов* — это флаг, который определяет, будет ли главное окно приложения отображаться в обычном режиме, развернуто или отображаться обычным образом.</span><span class="sxs-lookup"><span data-stu-id="1e987-112">*nCmdShow* is a flag that says whether the main application window will be minimized, maximized, or shown normally.</span></span>

<span data-ttu-id="1e987-113">Функция возвращает значение **типа int** .</span><span class="sxs-lookup"><span data-stu-id="1e987-113">The function returns an **int** value.</span></span> <span data-ttu-id="1e987-114">Возвращаемое значение не используется операционной системой, но можно использовать возвращаемое значение для передачи кода состояния другой программе, которую вы пишете.</span><span class="sxs-lookup"><span data-stu-id="1e987-114">The return value is not used by the operating system, but you can use the return value to convey a status code to some other program that you write.</span></span>

<span data-ttu-id="1e987-115">**WinAPI** — это соглашение о вызовах.</span><span class="sxs-lookup"><span data-stu-id="1e987-115">**WINAPI** is the calling convention.</span></span> <span data-ttu-id="1e987-116">*Соглашение о вызовах* определяет, как функция получает параметры от вызывающего.</span><span class="sxs-lookup"><span data-stu-id="1e987-116">A *calling convention* defines how a function receives parameters from the caller.</span></span> <span data-ttu-id="1e987-117">Например, он определяет порядок, в котором параметры отображаются в стеке.</span><span class="sxs-lookup"><span data-stu-id="1e987-117">For example, it defines the order that parameters appear on the stack.</span></span> <span data-ttu-id="1e987-118">Просто убедитесь, что вы объявили функцию **wWinMain** , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="1e987-118">Just make sure to declare your **wWinMain** function as shown.</span></span>

<span data-ttu-id="1e987-119">Функция **WinMain** идентична функции **wWinMain**, за исключением того, что аргументы командной строки передаются как строка ANSI.</span><span class="sxs-lookup"><span data-stu-id="1e987-119">The **WinMain** function is identical to **wWinMain**, except the command-line arguments are passed as an ANSI string.</span></span> <span data-ttu-id="1e987-120">Предпочтительнее использовать версию Юникода.</span><span class="sxs-lookup"><span data-stu-id="1e987-120">The Unicode version is preferred.</span></span> <span data-ttu-id="1e987-121">Функцию ANSI **WinMain** можно использовать, даже если вы компилируете программу в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="1e987-121">You can use the ANSI **WinMain** function even if you compile your program as Unicode.</span></span> <span data-ttu-id="1e987-122">Чтобы получить копию аргументов командной строки в Юникоде, вызовите функцию [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) .</span><span class="sxs-lookup"><span data-stu-id="1e987-122">To get a Unicode copy of the command-line arguments, call the [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) function.</span></span> <span data-ttu-id="1e987-123">Эта функция возвращает все аргументы в одной строке.</span><span class="sxs-lookup"><span data-stu-id="1e987-123">This function returns all of the arguments in a single string.</span></span> <span data-ttu-id="1e987-124">Если вы хотите, чтобы аргументы были в виде массива в стиле *argv*, передайте эту строку в [**коммандлинетоаргвв**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).</span><span class="sxs-lookup"><span data-stu-id="1e987-124">If you want the arguments as an *argv*-style array, pass this string to [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).</span></span>

<span data-ttu-id="1e987-125">Как компилятор узнает, что следует вызвать **wWinMain** вместо стандартной функции **Main** ?</span><span class="sxs-lookup"><span data-stu-id="1e987-125">How does the compiler know to invoke **wWinMain** instead of the standard **main** function?</span></span> <span data-ttu-id="1e987-126">В действительности библиотека времени выполнения Microsoft C (CRT) предоставляет реализацию **Main** , которая вызывает **WinMain** или **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="1e987-126">What actually happens is that the Microsoft C runtime library (CRT) provides an implementation of **main** that calls either **WinMain** or **wWinMain**.</span></span>

> [!Note]  
> <span data-ttu-id="1e987-127">CRT выполняет некоторую дополнительную работу внутри **Main**.</span><span class="sxs-lookup"><span data-stu-id="1e987-127">The CRT does some additional work inside **main**.</span></span> <span data-ttu-id="1e987-128">Например, все статические инициализаторы вызываются до **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="1e987-128">For example, any static initializers are called before **wWinMain**.</span></span> <span data-ttu-id="1e987-129">Несмотря на то, что компоновщик может использовать другую функцию точки входа, используйте значение по умолчанию при компоновке с CRT.</span><span class="sxs-lookup"><span data-stu-id="1e987-129">Although you can tell the linker to use a different entry-point function, use the default if you link to the CRT.</span></span> <span data-ttu-id="1e987-130">В противном случае код инициализации CRT будет пропущен с непредсказуемыми результатами.</span><span class="sxs-lookup"><span data-stu-id="1e987-130">Otherwise, the CRT initialization code will be skipped, with unpredictable results.</span></span> <span data-ttu-id="1e987-131">(Например, глобальные объекты не будут инициализированы должным образом.)</span><span class="sxs-lookup"><span data-stu-id="1e987-131">(For example, global objects will not be initialized correctly.)</span></span>

 

<span data-ttu-id="1e987-132">Ниже приведена пустая функция **WinMain** .</span><span class="sxs-lookup"><span data-stu-id="1e987-132">Here is an empty **WinMain** function.</span></span>


```C++
INT WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance,
    PSTR lpCmdLine, INT nCmdShow)
{
    return 0;
}
```



<span data-ttu-id="1e987-133">Теперь, когда у вас есть точка входа и вы понимаете некоторые основные термины по терминологии и программированию, можно приступать к созданию полной программы Window.</span><span class="sxs-lookup"><span data-stu-id="1e987-133">Now that you have the entry point and understand some of the basic terminology and coding conventions, you are ready to create a complete Window program.</span></span>

## <a name="next"></a><span data-ttu-id="1e987-134">Следующая</span><span class="sxs-lookup"><span data-stu-id="1e987-134">Next</span></span>

<span data-ttu-id="1e987-135">[Модуль 1. Ваша первая программа Windows](your-first-windows-program.md).</span><span class="sxs-lookup"><span data-stu-id="1e987-135">[Module 1. Your First Windows Program](your-first-windows-program.md).</span></span>

 

 
