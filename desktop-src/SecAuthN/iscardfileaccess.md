---
description: Следующее определение интерфейса предоставляется в качестве стандарта, который может быть выполнен при разработке поставщика услуг смарт-карты.
ms.assetid: 68cc0bbe-ce8e-4da1-b907-596caa95a39c
title: Интерфейс Искардфилеакцесс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess
api_type:
- COM
api_location: ''
ms.openlocfilehash: fcfcdc75bcf10b922a242574bfabe267c949fa52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910876"
---
# <a name="iscardfileaccess-interface"></a><span data-ttu-id="2d8bf-103">Интерфейс Искардфилеакцесс</span><span class="sxs-lookup"><span data-stu-id="2d8bf-103">ISCardFileAccess interface</span></span>

<span data-ttu-id="2d8bf-104">\[Интерфейс **искардфилеакцесс** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-104">\[The **ISCardFileAccess** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2d8bf-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2d8bf-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="2d8bf-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2d8bf-107">Следующее определение интерфейса предоставляется в качестве стандарта, который может быть выполнен при разработке [*поставщика услуг*](../secgloss/c-gly.md) [*смарт-карты*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="2d8bf-107">The following interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="2d8bf-108">Интерфейс **искардфилеакцесс** можно использовать для реализации высокоуровневого интерфейса для файловой системы на основе карт с базовой файловой системой карт, основанной на структуре, определенной в ISO/IEC 7816-4.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-108">The **ISCardFileAccess** interface can be used to implement a high-level interface to a card-based file system with an underlying card file system based on the structure defined in ISO/IEC 7816-4.</span></span> <span data-ttu-id="2d8bf-109">Возможны и другие реализации, но это будет наиболее распространенным.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-109">Other implementations are possible, but this is expected to be the most common.</span></span>

<span data-ttu-id="2d8bf-110">Интерфейс **искардфилеакцесс** можно использовать для предоставления сущностей файловой системы удобным для разработчиков приложениями в среде ПК.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-110">The **ISCardFileAccess** interface can be used to expose file system entities in a manner very familiar to application developers in the PC environment.</span></span> <span data-ttu-id="2d8bf-111">Он предоставляет механизмы для поиска конкретных файлов и выполнения общих операций, таких как выбор, чтение, запись, создание и удаление.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-111">It provides mechanisms for locating specific files and performing common operations such as selecting, reading, writing, creating and deleting.</span></span> <span data-ttu-id="2d8bf-112">Он инкапсулирует и маскирует большую часть подробностей, связанных с выполнением этих операций на уровне карты.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-112">It encapsulates and masks much of the low-level detail involved in performing these operations at the card level.</span></span>

<span data-ttu-id="2d8bf-113">Ниже приведен типичный пример использования интерфейса **искардфилеакцесс** .</span><span class="sxs-lookup"><span data-stu-id="2d8bf-113">Following is a typical use of the **ISCardFileAccess** interface.</span></span> <span data-ttu-id="2d8bf-114">В этом случае интерфейс **искардфилеакцесс** используется для выбора, открытия и записи в файл.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-114">In this case, the **ISCardFileAccess** interface is used to select, open, and write to a file.</span></span>

<span data-ttu-id="2d8bf-115">**Запись в файл**</span><span class="sxs-lookup"><span data-stu-id="2d8bf-115">**To write to a file**</span></span>

1.  <span data-ttu-id="2d8bf-116">Вызовите метод [**искардманаже:: креатефилеакцесс**](iscardmanage-createfileaccess.md) , чтобы создать интерфейс **искардфилеакцесс** .</span><span class="sxs-lookup"><span data-stu-id="2d8bf-116">Call [**ISCardManage::CreateFileAccess**](iscardmanage-createfileaccess.md) to create an **ISCardFileAccess** interface.</span></span>
2.  <span data-ttu-id="2d8bf-117">Вызовите [**Open**](iscardfileaccess-open.md) , чтобы выбрать и открыть файл.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-117">Call [**Open**](iscardfileaccess-open.md) to select and open the file.</span></span>
3.  <span data-ttu-id="2d8bf-118">Вызовите [**Write**](iscardfileaccess-write.md).</span><span class="sxs-lookup"><span data-stu-id="2d8bf-118">Call [**Write**](iscardfileaccess-write.md).</span></span>
4.  <span data-ttu-id="2d8bf-119">Вызов функции [**Close**](iscardfileaccess-close.md).</span><span class="sxs-lookup"><span data-stu-id="2d8bf-119">Call [**Close**](iscardfileaccess-close.md).</span></span>
5.  <span data-ttu-id="2d8bf-120">Освободите интерфейс **искардфилеакцесс** .</span><span class="sxs-lookup"><span data-stu-id="2d8bf-120">Release the **ISCardFileAccess** interface.</span></span>

## <a name="members"></a><span data-ttu-id="2d8bf-121">Элементы</span><span class="sxs-lookup"><span data-stu-id="2d8bf-121">Members</span></span>

<span data-ttu-id="2d8bf-122">Интерфейс **искардфилеакцесс** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="2d8bf-122">The **ISCardFileAccess** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="2d8bf-123">**Искардфилеакцесс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2d8bf-123">**ISCardFileAccess** also has these types of members:</span></span>

-   [<span data-ttu-id="2d8bf-124">Методы</span><span class="sxs-lookup"><span data-stu-id="2d8bf-124">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2d8bf-125">Методы</span><span class="sxs-lookup"><span data-stu-id="2d8bf-125">Methods</span></span>

<span data-ttu-id="2d8bf-126">Интерфейс **искардфилеакцесс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-126">The **ISCardFileAccess** interface has these methods.</span></span>



| <span data-ttu-id="2d8bf-127">Метод</span><span class="sxs-lookup"><span data-stu-id="2d8bf-127">Method</span></span>                                                              | <span data-ttu-id="2d8bf-128">Описание</span><span class="sxs-lookup"><span data-stu-id="2d8bf-128">Description</span></span>                                                                                                                                  |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d8bf-129">**чанжедир**</span><span class="sxs-lookup"><span data-stu-id="2d8bf-129">**ChangeDir**</span></span>](iscardfileaccess-changedir.md)                     | <span data-ttu-id="2d8bf-130">Изменяет текущий каталог смарт-карт на новый указанный каталог.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-130">Changes the current smart card directory to the new specified directory.</span></span><br/>                                                          |
| [<span data-ttu-id="2d8bf-131">**Закрыть**</span><span class="sxs-lookup"><span data-stu-id="2d8bf-131">**Close**</span></span>](iscardfileaccess-close.md)                             | <span data-ttu-id="2d8bf-132">Закрывает указанный файл.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-132">Closes the specified file.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="2d8bf-133">**Создать**</span><span class="sxs-lookup"><span data-stu-id="2d8bf-133">**Create**</span></span>](iscardfileaccess-create.md)                           | <span data-ttu-id="2d8bf-134">Создает файл в заданном месте в файловой системе ICC.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-134">Creates a file at a given location within the ICC file system.</span></span><br/>                                                                    |
| [<span data-ttu-id="2d8bf-135">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="2d8bf-135">**Delete**</span></span>](iscardfileaccess-delete.md)                           | <span data-ttu-id="2d8bf-136">Удаляет указанный файл.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-136">Deletes a specified file.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="2d8bf-137">**Каталог**</span><span class="sxs-lookup"><span data-stu-id="2d8bf-137">**Directory**</span></span>](iscardfileaccess-directory.md)                     | <span data-ttu-id="2d8bf-138">Извлекает список файлов.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-138">Retrieves a list of files.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="2d8bf-139">**жеткуррентдир**</span><span class="sxs-lookup"><span data-stu-id="2d8bf-139">**GetCurrentDir**</span></span>](iscardfileaccess-getcurrentdir.md)             | <span data-ttu-id="2d8bf-140">Возвращает абсолютный путь к выбранному в данный момент каталогу.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-140">Returns an absolute path to the currently selected directory.</span></span><br/>                                                                     |
| [<span data-ttu-id="2d8bf-141">**жетфилекапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="2d8bf-141">**GetFileCapabilities**</span></span>](iscardfileaccess-getfilecapabilities.md) | <span data-ttu-id="2d8bf-142">Получает возможности файла.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-142">Retrieves file capabilities.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="2d8bf-143">**GetProperties**</span><span class="sxs-lookup"><span data-stu-id="2d8bf-143">**GetProperties**</span></span>](iscardfileaccess-getproperties.md)             | <span data-ttu-id="2d8bf-144">Извлекает примитивные данные, на которые ссылаются теги, для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-144">Retrieves the primitive data referred by tags for the specified object.</span></span><br/>                                                           |
| [<span data-ttu-id="2d8bf-145">**Недействительным**</span><span class="sxs-lookup"><span data-stu-id="2d8bf-145">**Invalidate**</span></span>](iscardfileaccess-invalidate.md)                   | <span data-ttu-id="2d8bf-146">Делает указанный файл недопустимым.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-146">Makes the specified file not valid.</span></span><br/>                                                                                               |
| [<span data-ttu-id="2d8bf-147">**Открыт**</span><span class="sxs-lookup"><span data-stu-id="2d8bf-147">**Open**</span></span>](iscardfileaccess-open.md)                               | <span data-ttu-id="2d8bf-148">Открывает указанный файл для дальнейшего использования.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-148">Opens the specified file for further use.</span></span><br/>                                                                                         |
| [<span data-ttu-id="2d8bf-149">**Просмотр**</span><span class="sxs-lookup"><span data-stu-id="2d8bf-149">**Read**</span></span>](iscardfileaccess-read.md)                               | <span data-ttu-id="2d8bf-150">Считывает и возвращает указанные данные из заданного файла.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-150">Reads and returns the specified data from a given file.</span></span><br/>                                                                           |
| [<span data-ttu-id="2d8bf-151">**рехабилитате**</span><span class="sxs-lookup"><span data-stu-id="2d8bf-151">**Rehabilitate**</span></span>](iscardfileaccess-rehabilitate.md)               | <span data-ttu-id="2d8bf-152">Делает файл (EF или DF), который был ранее сделан недопустимым, с помощью команды unvalidate, доступной приложению.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-152">Makes a file (EF or DF), which has been previously made not valid by using the Invalidate command, accessible by the application.</span></span><br/> |
| [<span data-ttu-id="2d8bf-153">**Seek**</span><span class="sxs-lookup"><span data-stu-id="2d8bf-153">**Seek**</span></span>](iscardfileaccess-seek.md)                               | <span data-ttu-id="2d8bf-154">Выбирает объект, из которого будет выполняться разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-154">Selects the object from which read/write permission will be done.</span></span><br/>                                                                 |
| [<span data-ttu-id="2d8bf-155">**SetProperties**</span><span class="sxs-lookup"><span data-stu-id="2d8bf-155">**SetProperties**</span></span>](iscardfileaccess-setproperties.md)             | <span data-ttu-id="2d8bf-156">Задает примитивные данные, на которые ссылаются теги для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-156">Sets the primitive data referred by tags for the specified object.</span></span><br/>                                                                |
| [<span data-ttu-id="2d8bf-157">**Будет**</span><span class="sxs-lookup"><span data-stu-id="2d8bf-157">**Write**</span></span>](iscardfileaccess-write.md)                             | <span data-ttu-id="2d8bf-158">Записывает данные в текущий открытый файл.</span><span class="sxs-lookup"><span data-stu-id="2d8bf-158">Writes data to a current opened file.</span></span><br/>                                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="2d8bf-159">Требования</span><span class="sxs-lookup"><span data-stu-id="2d8bf-159">Requirements</span></span>



| <span data-ttu-id="2d8bf-160">Требование</span><span class="sxs-lookup"><span data-stu-id="2d8bf-160">Requirement</span></span> | <span data-ttu-id="2d8bf-161">Значение</span><span class="sxs-lookup"><span data-stu-id="2d8bf-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2d8bf-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d8bf-162">Minimum supported client</span></span><br/> | <span data-ttu-id="2d8bf-163">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2d8bf-163">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2d8bf-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d8bf-164">Minimum supported server</span></span><br/> | <span data-ttu-id="2d8bf-165">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2d8bf-165">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2d8bf-166">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2d8bf-166">End of client support</span></span><br/>    | <span data-ttu-id="2d8bf-167">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2d8bf-167">Windows XP</span></span><br/>                                |
| <span data-ttu-id="2d8bf-168">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="2d8bf-168">End of server support</span></span><br/>    | <span data-ttu-id="2d8bf-169">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2d8bf-169">Windows Server 2003</span></span><br/>                       |



 

 
