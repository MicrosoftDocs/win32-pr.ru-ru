---
description: Интерфейс Иинсталлатионресулт определяет следующие свойства.
ms.assetid: bd6cd5ae-2e43-4ac3-8ce7-ac80b7fc5cb8
title: Свойства Иинсталлатионресулт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78783b6758ab30d6a77c07cd71111486f3a7343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072806"
---
# <a name="iinstallationresult-properties"></a><span data-ttu-id="70a02-103">Свойства Иинсталлатионресулт</span><span class="sxs-lookup"><span data-stu-id="70a02-103">IInstallationResult Properties</span></span>

<span data-ttu-id="70a02-104">Интерфейс [**иинсталлатионресулт**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult) определяет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="70a02-104">The [**IInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult) interface defines the following properties.</span></span>



| <span data-ttu-id="70a02-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="70a02-105">Property</span></span>                                                     | <span data-ttu-id="70a02-106">Описание</span><span class="sxs-lookup"><span data-stu-id="70a02-106">Description</span></span>                                                                                                                            |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70a02-107">**Состав**</span><span class="sxs-lookup"><span data-stu-id="70a02-107">**HResult**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_hresult)               | <span data-ttu-id="70a02-108">Возвращает **значение HRESULT** исключения (при его наличии), которое возникает во время установки.</span><span class="sxs-lookup"><span data-stu-id="70a02-108">Gets the **HRESULT** of the exception, if any, that is raised during the installation.</span></span>                                                 |
| [<span data-ttu-id="70a02-109">**RebootRequired**</span><span class="sxs-lookup"><span data-stu-id="70a02-109">**RebootRequired**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_rebootrequired) | <span data-ttu-id="70a02-110">Возвращает логическое значение, указывающее, требуется ли перезагрузка компьютера для завершения установки или удаления обновления.</span><span class="sxs-lookup"><span data-stu-id="70a02-110">Gets a Boolean value that indicates whether you must restart the computer to complete the installation or uninstallation of an update.</span></span> |
| [<span data-ttu-id="70a02-111">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="70a02-111">**ResultCode**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_resultcode)         | <span data-ttu-id="70a02-112">Возвращает значение [**оператионресулткоде**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) , указывающее результат операции над обновлением.</span><span class="sxs-lookup"><span data-stu-id="70a02-112">Gets an [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) value that specifies the result of an operation on an update.</span></span>               |



 

 

 



