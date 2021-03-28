---
description: В этом разделе объясняется, как зарегистрировать обработчик просмотра, связанный с данным типом данных.
ms.assetid: 5f194d29-d09f-4426-a63e-911db65ce700
title: Регистрация обработчика просмотра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5af9610de1822678521557fc20aa53f4e556e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985420"
---
# <a name="how-to-register-a-preview-handler"></a><span data-ttu-id="78f01-103">Регистрация обработчика просмотра</span><span class="sxs-lookup"><span data-stu-id="78f01-103">How to Register a Preview Handler</span></span>

<span data-ttu-id="78f01-104">В этом разделе объясняется, как зарегистрировать обработчик просмотра, связанный с данным типом данных.</span><span class="sxs-lookup"><span data-stu-id="78f01-104">This topic explains how to register a preview handler associated with a given data type.</span></span> <span data-ttu-id="78f01-105">В примерах, приведенных в этом разделе, используется тип файла. xyz.</span><span class="sxs-lookup"><span data-stu-id="78f01-105">For the purposes of illustration, examples in this topic use a .xyz file type.</span></span> <span data-ttu-id="78f01-106">Регистрация обработчика просмотра — это Стандартная регистрация на основе сопоставления файлов.</span><span class="sxs-lookup"><span data-stu-id="78f01-106">Registration of a preview handler is a standard file association-based registration.</span></span>

## <a name="instructions"></a><span data-ttu-id="78f01-107">Инструкции</span><span class="sxs-lookup"><span data-stu-id="78f01-107">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="78f01-108">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="78f01-108">Step 1:</span></span>

<span data-ttu-id="78f01-109">Во-первых, расширение имени файла связано с ProgID.</span><span class="sxs-lookup"><span data-stu-id="78f01-109">First, a file name extension is associated with a ProgID.</span></span> <span data-ttu-id="78f01-110">Следующая запись связывает подраздел ProgID **ксизфиле** с расширением имени файла. xyz.</span><span class="sxs-lookup"><span data-stu-id="78f01-110">The following entry associates the **xyzfile** ProgID subkey with the .xyz file name extension.</span></span>

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = [REG_SZ] xyzfile
```

<span data-ttu-id="78f01-111">Подраздел ProgID **ксизфиле** хранится вместе с другими идентификаторами ProgID, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="78f01-111">The **xyzfile** ProgID subkey is stored with the other ProgIDs as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   xyzfile
```

<span data-ttu-id="78f01-112">Каждый подраздел ProgID обработчика просмотра содержит подраздел с именем **шеллекс** , *содержащий подраздел с* именем **{8895b1c6-b41f-4c1c-A562-0d564250836f}**.</span><span class="sxs-lookup"><span data-stu-id="78f01-112">Each preview handler ProgID subkey contains a subkey named **shellex** that contains a subkey *always* named **{8895b1c6-b41f-4c1c-a562-0d564250836f}**.</span></span> <span data-ttu-id="78f01-113">Наличие этого подраздела сообщает системе, что обработчик является обработчиком просмотра.</span><span class="sxs-lookup"><span data-stu-id="78f01-113">The presence of that subkey tells the system that the handler is a preview handler.</span></span>

<span data-ttu-id="78f01-114">Значение по умолчанию для подраздела **{8895b1c6-b41f-4c1c-A562-0d564250836f}** — это идентификатор класса (CLSID) обработчика.</span><span class="sxs-lookup"><span data-stu-id="78f01-114">The default value of the **{8895b1c6-b41f-4c1c-a562-0d564250836f}** subkey is the class identifier (CLSID) of your handler.</span></span> <span data-ttu-id="78f01-115">Ниже показан пример подраздела ProgID **ксизфиле** , связывающего обработчик CLSID {ec3a629a-a47c-4245-bc78-b4b63d0e3154}.</span><span class="sxs-lookup"><span data-stu-id="78f01-115">An example of the **xyzfile** ProgID subkey is shown here, associating a handler of CLSID {ec3a629a-a47c-4245-bc78-b4b63d0e3154}.</span></span>

```
HKEY_CLASSES_ROOT
   xyzfile
      shellex
         {8895b1c6-b41f-4c1c-a562-0d564250836f}
            (Default) = [REG_SZ] {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
```

### <a name="step-2"></a><span data-ttu-id="78f01-116">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="78f01-116">Step 2:</span></span>

<span data-ttu-id="78f01-117">Затем добавьте подраздел в **идентификатор CLSID** для обработчика просмотра.</span><span class="sxs-lookup"><span data-stu-id="78f01-117">Next, add the subkey under **CLSID** for your preview handler.</span></span> <span data-ttu-id="78f01-118">Пример показан здесь.</span><span class="sxs-lookup"><span data-stu-id="78f01-118">An example is shown here.</span></span> <span data-ttu-id="78f01-119">Ниже приведено описание отдельных записей.</span><span class="sxs-lookup"><span data-stu-id="78f01-119">An explanation of individual entries follows.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
         (Default) = [REG_SZ] Fabricam XYZ Preview Handler
         DisplayName = [REG_SZ] @myhandler.dll,-101
         Icon = [REG_SZ] myhandler.dll,201
         AppID = [REG_SZ] {6d2b5079-2f0b-48dd-ab7f-97cec514d30b}
         InprocServer32
            (Default) = [REG_EXPAND_SZ] %ProgramFiles%\Fabricam\myhandler.dll
            ThreadingModel = [REG_SZ] Apartment
            ProgID = [REG_SZ] xyzfile
            VersionIndependentProgID = [REG_SZ] Version IndependentProgID
```

<span data-ttu-id="78f01-120">Значение по умолчанию для подраздела (здесь **{ec3a629a-a47c-4245-bc78-b4b63d0e3154}**) не является обязательным или не используется.</span><span class="sxs-lookup"><span data-stu-id="78f01-120">The default value for your subkey (here, **{ec3a629a-a47c-4245-bc78-b4b63d0e3154}**) is not required or used.</span></span> <span data-ttu-id="78f01-121">Однако нелокализованная строка может помочь при отладке проблем с регистрацией.</span><span class="sxs-lookup"><span data-stu-id="78f01-121">However, setting it to a nonlocalized string can help you to debug registration issues.</span></span>

<span data-ttu-id="78f01-122">Знак "минус" (-101) в ресурсе. dll в записи DisplayName существует по причинам, существующим в предыдущих версиях.</span><span class="sxs-lookup"><span data-stu-id="78f01-122">The minus sign (-101) in the .dll resource in the DisplayName entry exists for legacy reasons.</span></span> <span data-ttu-id="78f01-123">В записи значка, с другой стороны, не требуется знак "минус".</span><span class="sxs-lookup"><span data-stu-id="78f01-123">The Icon entry, on the other hand, does not require a minus sign.</span></span>

<span data-ttu-id="78f01-124">Значение AppID дает ссылку на идентификатор приложения, связанный с расширением имени файла (хранится в **\_ \_ каталоге hKey root** \\ **AppID**.</span><span class="sxs-lookup"><span data-stu-id="78f01-124">The AppID value gives a reference to the AppID of the application associated with the file name extension (stored under **HKEY\_CLASSES\_ROOT**\\**APPID**.</span></span> <span data-ttu-id="78f01-125">Используемое здесь значение — {6d2b5079-2f0b-48dd-ab7f-97cec514d30b} — это идентификатор узла суррогата Prevhost.exe.</span><span class="sxs-lookup"><span data-stu-id="78f01-125">The value used here—{6d2b5079-2f0b-48dd-ab7f-97cec514d30b}—is the ID of the Prevhost.exe surrogate host.</span></span> <span data-ttu-id="78f01-126">32-разрядные обработчики просмотра должны использовать **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} при установке в 64-разрядных операционных системах.</span><span class="sxs-lookup"><span data-stu-id="78f01-126">32-bit preview handlers should use **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} when installed on 64-bit operating systems.</span></span>

<span data-ttu-id="78f01-127">Записи в подразделе **InprocServer32** содержат ссылку на подраздел ProgID для расширения имени файла, а также запись для [версиониндепендентпрогид](../com/versionindependentprogid.md).</span><span class="sxs-lookup"><span data-stu-id="78f01-127">The entries under the **InprocServer32** subkey include a reference back to the file name extension's ProgID subkey as well as an entry for a [VersionIndependentProgID](../com/versionindependentprogid.md).</span></span>

### <a name="step-3"></a><span data-ttu-id="78f01-128">Шаг 3.</span><span class="sxs-lookup"><span data-stu-id="78f01-128">Step 3:</span></span>

<span data-ttu-id="78f01-129">Наконец, обработчик просмотра должен быть добавлен в список всех обработчиков просмотра.</span><span class="sxs-lookup"><span data-stu-id="78f01-129">Finally, the preview handler must be added to the list of all preview handlers.</span></span> <span data-ttu-id="78f01-130">Этот список используется в качестве оптимизации системой для перечисления всех зарегистрированных обработчиков просмотра в целях показа.</span><span class="sxs-lookup"><span data-stu-id="78f01-130">This list is used as an optimization by the system to enumerate all registered preview handlers for display purposes.</span></span> <span data-ttu-id="78f01-131">Опять же, значение по умолчанию не является обязательным, оно просто помогает в процессе отладки.</span><span class="sxs-lookup"><span data-stu-id="78f01-131">Again, the default value is not required, it simply aids in the debugging process.</span></span>

> [!Note]  
> <span data-ttu-id="78f01-132">В Windows 7, если приложение установлено для всех пользователей компьютера, используйте HKEY \_ локальный \_ компьютер; если только для одного пользователя используйте hKey \_ текущий \_ пользователь.</span><span class="sxs-lookup"><span data-stu-id="78f01-132">In Windows 7, if the application is installed for all users of the computer, use HKEY\_LOCAL\_MACHINE; if for only one user, use HKEY\_CURRENT\_USER.</span></span>

 

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PreviewHandlers
                  {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
                     (Default) = [REG_SZ] Fabricam XYZ Preview Handler
```

## <a name="related-topics"></a><span data-ttu-id="78f01-133">См. также</span><span class="sxs-lookup"><span data-stu-id="78f01-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78f01-134">Обработчик предварительной версии и узел предварительной версии оболочки</span><span class="sxs-lookup"><span data-stu-id="78f01-134">Preview Handlers and Shell Preview Host</span></span>](preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="78f01-135">Создание обработчиков предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="78f01-135">Building Preview Handlers</span></span>](building-preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="78f01-136">Рекомендации по обработчику предварительной версии</span><span class="sxs-lookup"><span data-stu-id="78f01-136">Preview Handler Guidelines</span></span>](preview-handler-guidelines.md)
</dt> </dl>

 

 
