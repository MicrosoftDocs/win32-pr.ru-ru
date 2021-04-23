---
description: Установщик Windows выполняет следующие действия во время удаления приложения, если пакет содержит изолированные компоненты. Обычно общий компонент \_ является библиотекой DLL, которая совместно используется приложениями-компонентами \_ и другими клиентскими исполняемыми файлами.
ms.assetid: 26343a01-9a06-43d5-bbe3-959faf51739d
title: Удаление изолированных компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf19769067230b82f68a35f7b9fbedcd1c56440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650966"
---
# <a name="removal-of-isolated-components"></a><span data-ttu-id="6a1d5-104">Удаление изолированных компонентов</span><span class="sxs-lookup"><span data-stu-id="6a1d5-104">Removal of Isolated Components</span></span>

<span data-ttu-id="6a1d5-105">Установщик Windows выполняет следующие действия во время удаления приложения, если пакет содержит изолированные компоненты.</span><span class="sxs-lookup"><span data-stu-id="6a1d5-105">Windows Installer performs the following actions during the removal of an application when the package contains isolated components.</span></span> <span data-ttu-id="6a1d5-106">Обычно общий компонент \_ является библиотекой DLL, которая совместно используется приложениями-компонентами \_ и другими клиентскими исполняемыми файлами.</span><span class="sxs-lookup"><span data-stu-id="6a1d5-106">Typically, Component\_Shared is a DLL that is shared by Component\_Application and other client executables.</span></span>

## <a name="uninstall"></a><span data-ttu-id="6a1d5-107">Удаление</span><span class="sxs-lookup"><span data-stu-id="6a1d5-107">Uninstall</span></span>

-   <span data-ttu-id="6a1d5-108">Удалите файлы компонента, \_ Общие из папки, содержащей приложение компонента, \_ только если \_ также удаляется приложение компонента.</span><span class="sxs-lookup"><span data-stu-id="6a1d5-108">Remove the files of Component\_Shared from the folder containing Component\_Application only if Component\_Application is also being removed.</span></span>
-   <span data-ttu-id="6a1d5-109">Если бит Мсидбкомпонентаттрибутесшареддллрефкаунт установлен в [таблице Component](component-table.md) , уменьшите значение refcount шареддлл.</span><span class="sxs-lookup"><span data-stu-id="6a1d5-109">If the msidbComponentAttributesSharedDllRefCount bit is set in the [Component table](component-table.md) decrement the SharedDLL refcount.</span></span>
-   <span data-ttu-id="6a1d5-110">Удалите. ЛОКАЛЬНЫЙ нулевой байтовый файл из папки, содержащей \_ приложение компонента.</span><span class="sxs-lookup"><span data-stu-id="6a1d5-110">Remove the .LOCAL zero-byte file from the folder containing Component\_Application.</span></span>
-   <span data-ttu-id="6a1d5-111">Удалить \_ приложение компонента из списка клиентов общего доступа к компоненту \_ .</span><span class="sxs-lookup"><span data-stu-id="6a1d5-111">Remove Component\_Application from the client list of Component\_Shared.</span></span>
-   <span data-ttu-id="6a1d5-112">Удалите все ресурсы \_ приложения компонента, как обычно.</span><span class="sxs-lookup"><span data-stu-id="6a1d5-112">Remove all of the resources of Component\_Application as usual.</span></span>

<span data-ttu-id="6a1d5-113">Если в списке клиентов для общего сетевого компонента остались другие продукты \_ :</span><span class="sxs-lookup"><span data-stu-id="6a1d5-113">If there are other products remaining on the client list of Component\_Shared:</span></span>

-   <span data-ttu-id="6a1d5-114">Не удалять файлы из общего расположения совместно используемого компонента \_ .</span><span class="sxs-lookup"><span data-stu-id="6a1d5-114">Remove no files from the shared location of Component\_Shared.</span></span>

<span data-ttu-id="6a1d5-115">Если значение refcount Шареддлл для \_ общего компонента равно 0 после уменьшения, или если другие оставшиеся клиенты компонента не имеют \_ общего доступа:</span><span class="sxs-lookup"><span data-stu-id="6a1d5-115">If the SharedDLL refcount for Component\_Shared is 0 after being decremented, or if there are no other remaining clients of Component\_Shared:</span></span>

-   <span data-ttu-id="6a1d5-116">Удалите файлы компонента, \_ Общие из общего расположения.</span><span class="sxs-lookup"><span data-stu-id="6a1d5-116">Remove the files of Component\_Shared from the shared location.</span></span>
-   <span data-ttu-id="6a1d5-117">Обработайте все действия по удалению в соответствии с этим компонентом.</span><span class="sxs-lookup"><span data-stu-id="6a1d5-117">Process all uninstall actions with respect to this component.</span></span>

 

 



