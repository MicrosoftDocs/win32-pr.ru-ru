---
description: Действие Инсталлодбк устанавливает драйверы, переводчики и источники данных в таблицу Одбкдривер, таблицу Одбктранслатор и таблицу Одбкдатасаурце.
ms.assetid: fbcf1fdc-5aef-4431-93fe-3ed02748b5ff
title: Действие Инсталлодбк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac9becd2a528646805f4201cfb415a6bc61bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684354"
---
# <a name="installodbc-action"></a><span data-ttu-id="b088e-103">Действие Инсталлодбк</span><span class="sxs-lookup"><span data-stu-id="b088e-103">InstallODBC Action</span></span>

<span data-ttu-id="b088e-104">Действие Инсталлодбк устанавливает драйверы, переводчики и источники данных в [таблицу одбкдривер](odbcdriver-table.md), [таблицу Одбктранслатор](odbctranslator-table.md)и [таблицу одбкдатасаурце](odbcdatasource-table.md).</span><span class="sxs-lookup"><span data-stu-id="b088e-104">The InstallODBC action installs the drivers, translators, and data sources in the [ODBCDriver Table](odbcdriver-table.md), [ODBCTranslator Table](odbctranslator-table.md), and [ODBCDataSource Table](odbcdatasource-table.md).</span></span> <span data-ttu-id="b088e-105">Если драйвер или переводчик уже существует, действие Инсталлодбк выполняет вызовы SQL, необходимые для установки.</span><span class="sxs-lookup"><span data-stu-id="b088e-105">If a driver or translator already exists, the InstallODBC action makes SQL calls necessary for the installation.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="b088e-106">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="b088e-106">Sequence Restrictions</span></span>

<span data-ttu-id="b088e-107">Действие Инсталлодбк не копирует и не удаляет файлы и должно быть после действий, которые копируют или удаляют файлы.</span><span class="sxs-lookup"><span data-stu-id="b088e-107">The InstallODBC action does not copy or remove files, and must be after actions that copy or remove files.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="b088e-108">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="b088e-108">ActionData Messages</span></span>

<span data-ttu-id="b088e-109">В следующей таблице указаны сообщения Актиондата для каждого установленного драйвера.</span><span class="sxs-lookup"><span data-stu-id="b088e-109">The following table identifies the ActionData messages for each installed driver.</span></span>



| <span data-ttu-id="b088e-110">Поле</span><span class="sxs-lookup"><span data-stu-id="b088e-110">Field</span></span>       | <span data-ttu-id="b088e-111">Описание</span><span class="sxs-lookup"><span data-stu-id="b088e-111">Description</span></span>                                                              |
|-------------|--------------------------------------------------------------------------|
| <span data-ttu-id="b088e-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="b088e-112">\[1\]</span></span>       | <span data-ttu-id="b088e-113">Описание драйвера.</span><span class="sxs-lookup"><span data-stu-id="b088e-113">Driver description.</span></span> <span data-ttu-id="b088e-114">Ключ драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="b088e-114">The ODBC driver key.</span></span>                                 |
| <span data-ttu-id="b088e-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="b088e-115">\[2\]</span></span>       | <span data-ttu-id="b088e-116">ComponentID.</span><span class="sxs-lookup"><span data-stu-id="b088e-116">ComponentId.</span></span>                                                             |
| <span data-ttu-id="b088e-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="b088e-117">\[3\]</span></span>       | <span data-ttu-id="b088e-118">Folder.</span><span class="sxs-lookup"><span data-stu-id="b088e-118">Folder.</span></span>                                                                  |
| <span data-ttu-id="b088e-119">\[4, 5,...\]</span><span class="sxs-lookup"><span data-stu-id="b088e-119">\[4, 5, …\]</span></span> | <span data-ttu-id="b088e-120">Пары атрибутов и значений из [одбкаттрибуте](odbcattribute-table.md).</span><span class="sxs-lookup"><span data-stu-id="b088e-120">Attribute and value pairs from [ODBCAttribute](odbcattribute-table.md).</span></span> |



 

<span data-ttu-id="b088e-121">В следующей таблице указаны сообщения Актиондата для каждого установленного транслятора.</span><span class="sxs-lookup"><span data-stu-id="b088e-121">The following table identifies the ActionData messages for each installed translator.</span></span>



| <span data-ttu-id="b088e-122">Поле</span><span class="sxs-lookup"><span data-stu-id="b088e-122">Field</span></span>       | <span data-ttu-id="b088e-123">Описание</span><span class="sxs-lookup"><span data-stu-id="b088e-123">Description</span></span>                                                              |
|-------------|--------------------------------------------------------------------------|
| <span data-ttu-id="b088e-124">\[1\]</span><span class="sxs-lookup"><span data-stu-id="b088e-124">\[1\]</span></span>       | <span data-ttu-id="b088e-125">Описание драйвера.</span><span class="sxs-lookup"><span data-stu-id="b088e-125">Driver description.</span></span> <span data-ttu-id="b088e-126">Ключ драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="b088e-126">The ODBC driver key.</span></span>                                 |
| <span data-ttu-id="b088e-127">\[2\]</span><span class="sxs-lookup"><span data-stu-id="b088e-127">\[2\]</span></span>       | <span data-ttu-id="b088e-128">ComponentID.</span><span class="sxs-lookup"><span data-stu-id="b088e-128">ComponentId.</span></span>                                                             |
| <span data-ttu-id="b088e-129">\[3\]</span><span class="sxs-lookup"><span data-stu-id="b088e-129">\[3\]</span></span>       | <span data-ttu-id="b088e-130">Folder.</span><span class="sxs-lookup"><span data-stu-id="b088e-130">Folder.</span></span>                                                                  |
| <span data-ttu-id="b088e-131">\[4, 5,...\]</span><span class="sxs-lookup"><span data-stu-id="b088e-131">\[4, 5, …\]</span></span> | <span data-ttu-id="b088e-132">Пары атрибутов и значений из [одбкаттрибуте](odbcattribute-table.md).</span><span class="sxs-lookup"><span data-stu-id="b088e-132">Attribute and value pairs from [ODBCAttribute](odbcattribute-table.md).</span></span> |



 

<span data-ttu-id="b088e-133">В следующей таблице указаны сообщения Актиондата для каждого установленного источника данных.</span><span class="sxs-lookup"><span data-stu-id="b088e-133">The following table identifies the ActionData messages for each installed data source.</span></span>



| <span data-ttu-id="b088e-134">Поле</span><span class="sxs-lookup"><span data-stu-id="b088e-134">Field</span></span>       | <span data-ttu-id="b088e-135">Описание</span><span class="sxs-lookup"><span data-stu-id="b088e-135">Description</span></span>                                                              |
|-------------|--------------------------------------------------------------------------|
| <span data-ttu-id="b088e-136">\[1\]</span><span class="sxs-lookup"><span data-stu-id="b088e-136">\[1\]</span></span>       | <span data-ttu-id="b088e-137">Описание драйвера.</span><span class="sxs-lookup"><span data-stu-id="b088e-137">Driver description.</span></span> <span data-ttu-id="b088e-138">Ключ драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="b088e-138">The ODBC driver key.</span></span>                                 |
| <span data-ttu-id="b088e-139">\[2\]</span><span class="sxs-lookup"><span data-stu-id="b088e-139">\[2\]</span></span>       | <span data-ttu-id="b088e-140">ComponentID.</span><span class="sxs-lookup"><span data-stu-id="b088e-140">ComponentId.</span></span>                                                             |
| <span data-ttu-id="b088e-141">\[3\]</span><span class="sxs-lookup"><span data-stu-id="b088e-141">\[3\]</span></span>       | <span data-ttu-id="b088e-142">Регистрация: ODBC \_ Add \_ DSN или ODBC \_ Add \_ sys \_ DSN.</span><span class="sxs-lookup"><span data-stu-id="b088e-142">Registration: ODBC\_ADD\_DSN or ODBC\_ADD\_SYS\_DSN.</span></span>                     |
| <span data-ttu-id="b088e-143">\[4, 5,...\]</span><span class="sxs-lookup"><span data-stu-id="b088e-143">\[4, 5, …\]</span></span> | <span data-ttu-id="b088e-144">Пары атрибутов и значений из [одбкаттрибуте](odbcattribute-table.md).</span><span class="sxs-lookup"><span data-stu-id="b088e-144">Attribute and value pairs from [ODBCAttribute](odbcattribute-table.md).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b088e-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b088e-145">Remarks</span></span>

<span data-ttu-id="b088e-146">Диспетчер драйверов ODBC должен быть создан в пакете установщика Microsoft, и должен быть добавлен компонент с именем Одбкдриверманажер.</span><span class="sxs-lookup"><span data-stu-id="b088e-146">The ODBC Driver Manager must be authored in the Microsoft Installer package and a component named ODBCDriverManager must be included.</span></span> <span data-ttu-id="b088e-147">При необходимости диспетчер устанавливается.</span><span class="sxs-lookup"><span data-stu-id="b088e-147">The manager is installed if necessary.</span></span>

<span data-ttu-id="b088e-148">Чтобы переименовать компонент, присвойте свойству с именем Одбкдриверманажер новое имя компонента.</span><span class="sxs-lookup"><span data-stu-id="b088e-148">To rename the component, set a property named ODBCDriverManager to the new name of the component.</span></span> <span data-ttu-id="b088e-149">Если требуется установить диспетчер драйверов ODBC 64, компонент, который его несет, должен называться ODBCDriverManager64.</span><span class="sxs-lookup"><span data-stu-id="b088e-149">If a 64-bit ODBC Driver Manager is to be installed, the component that carries it should be named ODBCDriverManager64.</span></span>

-   <span data-ttu-id="b088e-150">Действие Инсталлодбк запрашивает [таблицу одбкдатасаурце](odbcdatasource-table.md) и [таблицу одбксаурцеаттрибуте](odbcsourceattribute-table.md) для каждого устанавливаемого источника данных и атрибуты источника данных.</span><span class="sxs-lookup"><span data-stu-id="b088e-150">The InstallODBC action queries the [ODBCDataSource Table](odbcdatasource-table.md) and the [ODBCSourceAttribute Table](odbcsourceattribute-table.md) for each data source to be installed, and the attributes of the data source.</span></span>
-   <span data-ttu-id="b088e-151">Действие Инсталлодбк запрашивает [таблицу одбкдривер](odbcdriver-table.md) и [таблицу одбктранслатор](odbctranslator-table.md) для каждого драйвера и переводчика, выбранного для установки.</span><span class="sxs-lookup"><span data-stu-id="b088e-151">The InstallODBC action queries the [ODBCDriver Table](odbcdriver-table.md) and the [ODBCTranslator Table](odbctranslator-table.md) for each driver and translator that is selected for installation.</span></span>
-   <span data-ttu-id="b088e-152">Действие Инсталлодбк запрашивает [таблицу одбкаттрибуте](odbcattribute-table.md) для атрибутов драйверов и переводчиков.</span><span class="sxs-lookup"><span data-stu-id="b088e-152">The InstallODBC action queries the [ODBCAttribute Table](odbcattribute-table.md) for the attributes of the drivers and translators.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b088e-153">См. также</span><span class="sxs-lookup"><span data-stu-id="b088e-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b088e-154">Примеры установщик Windows</span><span class="sxs-lookup"><span data-stu-id="b088e-154">Windows Installer Examples</span></span>](windows-installer-examples.md)
</dt> </dl>

 

 



