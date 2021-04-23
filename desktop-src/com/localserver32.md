---
title: LocalServer32
description: Указывает полный путь к 32-битному локальному серверному приложению.
ms.assetid: 5d922230-f53d-4bf9-be50-c8c00f45b7a8
keywords:
- COM-код раздела реестра LocalServer32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd068f51f33b6c283384198c0206bc9c3b6357f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104533551"
---
# <a name="localserver32"></a><span data-ttu-id="46c63-104">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="46c63-104">LocalServer32</span></span>

<span data-ttu-id="46c63-105">Указывает полный путь к 32-битному локальному серверному приложению.</span><span class="sxs-lookup"><span data-stu-id="46c63-105">Specifies the full path to a 32-bit local server application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="46c63-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="46c63-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer32
         (Default) = path
         ServerExecutable = path
```

## <a name="remarks"></a><span data-ttu-id="46c63-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46c63-107">Remarks</span></span>

<span data-ttu-id="46c63-108">Значение **серверексекутабле** , которое имеет тип **reg \_ SZ** и поддерживается начиная с Windows Server 2003, работает в сочетании с подразделом **LocalServer32** для предотвращения неоднозначности при использовании функции [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="46c63-108">The **ServerExecutable** value, which is of type **REG\_SZ** and is supported starting with Windows Server 2003, works in conjunction with the **LocalServer32** subkey to prevent any ambiguity when using the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span> <span data-ttu-id="46c63-109">**LocalServer32** указывает расположение приложения COM-сервера для запуска, и эти сведения передаются в качестве первого параметра *лпаппликатионнаме* для **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="46c63-109">**LocalServer32** specifies the location of the COM server application to launch, and this information is passed as the first parameter *lpApplicationName* for **CreateProcess**.</span></span> <span data-ttu-id="46c63-110">В зависимости от реализации **CreateProcess** эта информация может быть неоднозначной.</span><span class="sxs-lookup"><span data-stu-id="46c63-110">Depending on the implementation of **CreateProcess**, this information might be ambiguous.</span></span> <span data-ttu-id="46c63-111">По этой причине, если указан **серверексекутабле** , com передает именованное значение **Серверексекутабле** в параметр *лпаппликатионнаме* **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="46c63-111">For this reason, if **ServerExecutable** is specified, COM passes the **ServerExecutable** named value to the *lpApplicationName* parameter of **CreateProcess**.</span></span> <span data-ttu-id="46c63-112">Если **серверексекутабле** не указан, com передает значение **null** в качестве значения для первого параметра **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="46c63-112">If **ServerExecutable** is not specified, COM passes **NULL** as the value for the first parameter of **CreateProcess**.</span></span>

<span data-ttu-id="46c63-113">Чтобы обеспечить безопасность системы, используйте заключенные в кавычки строки в пути, чтобы указать, где заканчивается имя исполняемого файла и начинаются аргументы.</span><span class="sxs-lookup"><span data-stu-id="46c63-113">To help provide system security, use quoted strings in the path to indicate where the executable filename ends and the arguments begin.</span></span> <span data-ttu-id="46c63-114">Например, вместо указания следующего пути в качестве записи **LocalServer32** :</span><span class="sxs-lookup"><span data-stu-id="46c63-114">For example, instead of specifying the following path as the **LocalServer32** entry:</span></span>

<span data-ttu-id="46c63-115">"C: \\ Program Files \\ файлы компании \\Application.exe Param1 Param2"</span><span class="sxs-lookup"><span data-stu-id="46c63-115">"C:\\Program Files\\Company Files\\Application.exe param1 param2"</span></span>

<span data-ttu-id="46c63-116">Укажите путь, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="46c63-116">specify the path using the following syntax:</span></span>

<span data-ttu-id="46c63-117">" \\ " C: \\ Program Files \\ файлы компании \\Application.exe\\ "param1 Param2"</span><span class="sxs-lookup"><span data-stu-id="46c63-117">"\\"C:\\Program Files\\Company Files\\Application.exe\\" param1 param2"</span></span>

<span data-ttu-id="46c63-118">COM добавляет к строке флаг "-Встраивание", поэтому приложение, использующее флаги, должно анализировать всю строку и проверять флаг-встраивание.</span><span class="sxs-lookup"><span data-stu-id="46c63-118">COM appends the "-Embedding" flag to the string, so the application that uses flags needs to parse the whole string and check for the -Embedding flag.</span></span>

<span data-ttu-id="46c63-119">Когда COM запускает 32-разрядный локальный сервер, сервер должен зарегистрировать объект класса в течение истекшего времени, установленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="46c63-119">When COM starts a 32-bit local server, the server must register a class object within an elapsed time set by the user.</span></span> <span data-ttu-id="46c63-120">По умолчанию значение затраченного времени должно быть не менее 5 минут в миллисекундах, но не может превышать число миллисекунд в 30 дней.</span><span class="sxs-lookup"><span data-stu-id="46c63-120">By default, the elapsed time value must be at least 5 minutes, in milliseconds, but cannot exceed the number of milliseconds in 30 days.</span></span> <span data-ttu-id="46c63-121">Приложениям обычно не следует задавать это значение, которое находится в записи **\_ \_ Microsoft COM2 на локальном компьютере в \\ \\ программе \\ \\ серверстартелапседтиме** .</span><span class="sxs-lookup"><span data-stu-id="46c63-121">Applications typically should not set this value, which is in the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\COM2\\ServerStartElapsedTime** entry.</span></span>

<span data-ttu-id="46c63-122">Обязательные записи для 32-разрядных локальных серверов: [**InprocHandler32**](inprochandler32.md), [**локалсервер**](localserver.md), **LocalServer32** и [**INSERT**](insertable.md).</span><span class="sxs-lookup"><span data-stu-id="46c63-122">The required entries for 32-bit local servers are [**InprocHandler32**](inprochandler32.md), [**LocalServer**](localserver.md), **LocalServer32**, and [**Insertable**](insertable.md).</span></span>

<span data-ttu-id="46c63-123">Если контейнер выполняет поиск в реестре для локального сервера, 32-битный локальный сервер имеет приоритет над 16-битным локальным сервером.</span><span class="sxs-lookup"><span data-stu-id="46c63-123">If a container is searching the registry for a local server, a 32-bit local server has priority over a 16-bit local server.</span></span>

<span data-ttu-id="46c63-124">При реализации классов в качестве служб следует иметь в виду, что именованное значение [**LocalService**](localservice.md) используется в предпочтениях к ключу **LocalServer32** для локальной и удаленной активации рекуестсâ € **"Если существует** и ссылается на допустимую службу, ключ **LocalServer32** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="46c63-124">If you are implementing classes as services, you should be aware that the [**LocalService**](localservice.md) named value is used in preference to the **LocalServer32** key for local and remote activation requestsâ€”if **LocalService** exists and refers to a valid service, the **LocalServer32** key is ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46c63-125">См. также</span><span class="sxs-lookup"><span data-stu-id="46c63-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46c63-126">**локалсервер**</span><span class="sxs-lookup"><span data-stu-id="46c63-126">**LocalServer**</span></span>](localserver.md)
</dt> <dt>

[<span data-ttu-id="46c63-127">**локальная служба.**</span><span class="sxs-lookup"><span data-stu-id="46c63-127">**LocalService**</span></span>](localservice.md)
</dt> </dl>

 

 