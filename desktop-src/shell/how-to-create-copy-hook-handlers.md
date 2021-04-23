---
description: Использование расширений оболочки для реализации обработчика ловушки копирования.
ms.assetid: 05808281-84fb-402d-9fa1-3a747b29d030
title: Как создавать обработчики обработчиков копий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1468839eacc10272f8f97a120b98ada6d580bacf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264424"
---
# <a name="how-to-create-copy-hook-handlers"></a><span data-ttu-id="b2216-103">Как создавать обработчики обработчиков копий</span><span class="sxs-lookup"><span data-stu-id="b2216-103">How to Create Copy Hook Handlers</span></span>

<span data-ttu-id="b2216-104">Общие процедуры для реализации и регистрации обработчика расширений оболочки обсуждаются в разделе [Создание обработчиков расширений оболочки](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="b2216-104">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="b2216-105">В этом документе рассматриваются аспекты реализации, характерные для обработчиков событий копирования.</span><span class="sxs-lookup"><span data-stu-id="b2216-105">This document focuses on those aspects of implementation that are specific to copy hook handlers.</span></span>

-   [<span data-ttu-id="b2216-106">Реализация обработчиков событий копирования</span><span class="sxs-lookup"><span data-stu-id="b2216-106">Implementing Copy Hook Handlers</span></span>](#step-1-implementing-copy-hook-handlers)
-   [<span data-ttu-id="b2216-107">Регистрация обработчиков событий копирования</span><span class="sxs-lookup"><span data-stu-id="b2216-107">Registering Copy Hook Handlers</span></span>](#step-2-registering-copy-hook-handlers)
-   [<span data-ttu-id="b2216-108">См. также</span><span class="sxs-lookup"><span data-stu-id="b2216-108">Related topics</span></span>](#related-topics)

## <a name="instructions"></a><span data-ttu-id="b2216-109">Инструкции</span><span class="sxs-lookup"><span data-stu-id="b2216-109">Instructions</span></span>

### <a name="step-1-implementing-copy-hook-handlers"></a><span data-ttu-id="b2216-110">Шаг 1. Реализация обработчиков событий копирования</span><span class="sxs-lookup"><span data-stu-id="b2216-110">Step 1: Implementing Copy Hook Handlers</span></span>

<span data-ttu-id="b2216-111">Как и все обработчики расширений оболочки, обработчики событий копирования — это объекты модели COM, реализованные в виде библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="b2216-111">Like all Shell extension handlers, copy hook handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="b2216-112">В дополнение к [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**икопихук**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)), они экспортируют один интерфейс.</span><span class="sxs-lookup"><span data-stu-id="b2216-112">They export one interface in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)).</span></span> <span data-ttu-id="b2216-113">Оболочка инициализирует обработчик напрямую, поэтому нет необходимости в интерфейсе инициализации, например [**ишеллекстинит**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit).</span><span class="sxs-lookup"><span data-stu-id="b2216-113">The Shell initializes the handler directly, so there is no need for an initialization interface such as [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit).</span></span>

<span data-ttu-id="b2216-114">Интерфейс [**икопихук**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)) содержит один метод [**Икопихук:: копикаллбакк**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b2216-114">The [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)) interface has a single method, [**ICopyHook::CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)).</span></span> <span data-ttu-id="b2216-115">Когда папка собирается для перемещения, оболочка вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="b2216-115">When a folder is about to be moved, the Shell calls this method.</span></span> <span data-ttu-id="b2216-116">Он передается в различные данные, в том числе:</span><span class="sxs-lookup"><span data-stu-id="b2216-116">It passes in a variety of information, including:</span></span>

-   <span data-ttu-id="b2216-117">Имя папки.</span><span class="sxs-lookup"><span data-stu-id="b2216-117">The folder's name.</span></span>
-   <span data-ttu-id="b2216-118">Место назначения папки или новое имя.</span><span class="sxs-lookup"><span data-stu-id="b2216-118">The folder's destination or new name.</span></span>
-   <span data-ttu-id="b2216-119">Попытка выполнить операцию.</span><span class="sxs-lookup"><span data-stu-id="b2216-119">The operation that is being attempted.</span></span>
-   <span data-ttu-id="b2216-120">Атрибуты исходной и целевой папок.</span><span class="sxs-lookup"><span data-stu-id="b2216-120">The attributes of the source and destination folders.</span></span>
-   <span data-ttu-id="b2216-121">Маркер окна, который может использоваться для вывода пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b2216-121">A window handle that can be used to display a user interface.</span></span>

<span data-ttu-id="b2216-122">Когда вызывается метод [**икопихук:: копикаллбакк**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) обработчика, он возвращает одно из трех следующих значений, чтобы указать оболочке, как она должна быть продолжена.</span><span class="sxs-lookup"><span data-stu-id="b2216-122">When your handler's [**ICopyHook::CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) method is called, it returns one of the three following values to indicate to the Shell how it should proceed.</span></span>



| <span data-ttu-id="b2216-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b2216-123">Value</span></span>    | <span data-ttu-id="b2216-124">Описание</span><span class="sxs-lookup"><span data-stu-id="b2216-124">Description</span></span>                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2216-125">IDYES</span><span class="sxs-lookup"><span data-stu-id="b2216-125">IDYES</span></span>    | <span data-ttu-id="b2216-126">Разрешает операцию.</span><span class="sxs-lookup"><span data-stu-id="b2216-126">Allows the operation.</span></span>                                                                                                                            |
| <span data-ttu-id="b2216-127">IDNO</span><span class="sxs-lookup"><span data-stu-id="b2216-127">IDNO</span></span>     | <span data-ttu-id="b2216-128">Предотвращает операцию в этой папке.</span><span class="sxs-lookup"><span data-stu-id="b2216-128">Prevents the operation on this folder.</span></span> <span data-ttu-id="b2216-129">Оболочка может продолжить работу с другими утвержденными операциями, например с операцией пакетного копирования.</span><span class="sxs-lookup"><span data-stu-id="b2216-129">The Shell can continue with any other operations that have been approved, such as a batch copy operation.</span></span> |
| <span data-ttu-id="b2216-130">IDCANCEL</span><span class="sxs-lookup"><span data-stu-id="b2216-130">IDCANCEL</span></span> | <span data-ttu-id="b2216-131">Предотвращает текущую операцию и отменяет все ожидающие операции.</span><span class="sxs-lookup"><span data-stu-id="b2216-131">Prevents the current operation and cancels any pending operations.</span></span>                                                                               |



 

### <a name="step-2-registering-copy-hook-handlers"></a><span data-ttu-id="b2216-132">Шаг 2. Регистрация обработчиков событий копирования</span><span class="sxs-lookup"><span data-stu-id="b2216-132">Step 2: Registering Copy Hook Handlers</span></span>

<span data-ttu-id="b2216-133">Обработчики событий копирования для папок регистрируются в подразделе шеллекс копихукхандлерс **\_ \_ корневого каталога классов hKey** \\  \\  \\  .</span><span class="sxs-lookup"><span data-stu-id="b2216-133">Copy hook handlers for folders are registered under the **HKEY\_CLASSES\_ROOT**\\**Directory**\\**shellex**\\**CopyHookHandlers** subkey.</span></span> <span data-ttu-id="b2216-134">Создайте подраздел **копихукхандлерс** с именем для обработчика и задайте в качестве значения по умолчанию для подраздела строковое значение GUID идентификатора класса обработчика (CLSID).</span><span class="sxs-lookup"><span data-stu-id="b2216-134">Create a subkey of **CopyHookHandlers** named for the handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span>

<span data-ttu-id="b2216-135">В следующем примере добавляется подраздел **микопихандлер** в список обработчиков дескрипторов копий оболочки.</span><span class="sxs-lookup"><span data-stu-id="b2216-135">The following example adds the **MyCopyHandler** subkey to the Shell's list of copy hook handlers.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         CopyHookHandlers
            MyCopyHandler
               (Default) = {MyCopyHandler CLSID GUID}
```

<span data-ttu-id="b2216-136">Обработчики событий копирования для объектов принтеров в основном регистрируются аналогичным образом.</span><span class="sxs-lookup"><span data-stu-id="b2216-136">Copy hook handlers for printer objects are registered in essentially the same way.</span></span> <span data-ttu-id="b2216-137">Единственное отличие заключается в том, что их необходимо зарегистрировать в подразделе " **\_ \_ корневые** \\ **принтеры** классов hKey".</span><span class="sxs-lookup"><span data-stu-id="b2216-137">The only difference is that you must register them under the **HKEY\_CLASSES\_ROOT**\\**Printers** subkey.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2216-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="b2216-138">Remarks</span></span>

<span data-ttu-id="b2216-139">Обычно пользователи и приложения могут копировать, перемещать, удалять или переименовывать папки с небольшими ограничениями.</span><span class="sxs-lookup"><span data-stu-id="b2216-139">Normally, users and applications can copy, move, delete, or rename folders with few restrictions.</span></span> <span data-ttu-id="b2216-140">Реализуя обработчик события копирования, вы можете контролировать, выполняются ли эти операции.</span><span class="sxs-lookup"><span data-stu-id="b2216-140">By implementing a copy hook handler, you can control whether these operations take place.</span></span> <span data-ttu-id="b2216-141">Например, реализация такого обработчика позволяет предотвратить переименование или удаление критических папок.</span><span class="sxs-lookup"><span data-stu-id="b2216-141">For instance, implementing such a handler allows you to prevent critical folders from being renamed or deleted.</span></span> <span data-ttu-id="b2216-142">Для объектов-принтеров также могут быть реализованы обработчики ловушек копирования.</span><span class="sxs-lookup"><span data-stu-id="b2216-142">Copy hook handlers can also be implemented for printer objects.</span></span>

<span data-ttu-id="b2216-143">Обработчики копирования являются глобальными.</span><span class="sxs-lookup"><span data-stu-id="b2216-143">Copy hook handlers are global.</span></span> <span data-ttu-id="b2216-144">Оболочка вызывает все зарегистрированные обработчики каждый раз, когда приложение или пользователь пытается скопировать, переместить, удалить или переименовать папку или объект принтера.</span><span class="sxs-lookup"><span data-stu-id="b2216-144">The Shell calls all registered handlers every time an application or user attempts to copy, move, delete, or rename a folder or printer object.</span></span> <span data-ttu-id="b2216-145">Обработчик не выполняет саму операцию.</span><span class="sxs-lookup"><span data-stu-id="b2216-145">The handler does not perform the operation itself.</span></span> <span data-ttu-id="b2216-146">Он только утверждает или отменяет его.</span><span class="sxs-lookup"><span data-stu-id="b2216-146">It only approves or vetoes it.</span></span> <span data-ttu-id="b2216-147">Если все обработчики утверждены, оболочка выполняет операцию.</span><span class="sxs-lookup"><span data-stu-id="b2216-147">If all handlers approve, the Shell does the operation.</span></span> <span data-ttu-id="b2216-148">Если какой-либо из обработчиков отменяет операцию, он отменяется и остальные обработчики не вызываются.</span><span class="sxs-lookup"><span data-stu-id="b2216-148">If any handler vetoes the operation, it is canceled and the remaining handlers are not called.</span></span> <span data-ttu-id="b2216-149">Обработчики событий копирования не сообщают об успехе или неуспешном выполнении операции, поэтому их нельзя использовать для наблюдения за операциями с файлами.</span><span class="sxs-lookup"><span data-stu-id="b2216-149">Copy hook handlers are not informed of the success or failure of the operation, so they cannot be used to monitor file operations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2216-150">См. также</span><span class="sxs-lookup"><span data-stu-id="b2216-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2216-151">Создание обработчиков расширений оболочки</span><span class="sxs-lookup"><span data-stu-id="b2216-151">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

<span data-ttu-id="b2216-152">[**икопихук**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b2216-152">[**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))</span></span>
</dt> </dl>

 

 
