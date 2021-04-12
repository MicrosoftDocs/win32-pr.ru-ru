---
description: Интерфейс Иупдатеинсталлатионресулт определяет следующие свойства.
ms.assetid: 7e8f7125-f89b-416f-bcc5-422eecabe0c4
title: Свойства Иупдатеинсталлатионресулт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27b2e2792215d8d927d6e6157c82e37193e74d2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263209"
---
# <a name="iupdateinstallationresult-properties"></a><span data-ttu-id="6f291-103">Свойства Иупдатеинсталлатионресулт</span><span class="sxs-lookup"><span data-stu-id="6f291-103">IUpdateInstallationResult Properties</span></span>

<span data-ttu-id="6f291-104">Интерфейс [**иупдатеинсталлатионресулт**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) определяет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6f291-104">The [**IUpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) interface defines the following properties.</span></span>



| <span data-ttu-id="6f291-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="6f291-105">Property</span></span>                                                           | <span data-ttu-id="6f291-106">Описание</span><span class="sxs-lookup"><span data-stu-id="6f291-106">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f291-107">**Состав**</span><span class="sxs-lookup"><span data-stu-id="6f291-107">**HResult**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_hresult)               | <span data-ttu-id="6f291-108">Возвращает значение исключения **HRESULT** , возникающее во время операции обновления.</span><span class="sxs-lookup"><span data-stu-id="6f291-108">Gets the **HRESULT** exception value that is raised during the operation on an update.</span></span>                                            |
| [<span data-ttu-id="6f291-109">**RebootRequired**</span><span class="sxs-lookup"><span data-stu-id="6f291-109">**RebootRequired**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_rebootrequired) | <span data-ttu-id="6f291-110">Возвращает логическое значение, указывающее, требуется ли перезагрузка системы на компьютере для завершения установки обновления.</span><span class="sxs-lookup"><span data-stu-id="6f291-110">Gets a Boolean value that indicates whether a system restart is required on a computer to complete the installation of an update.</span></span> |
| [<span data-ttu-id="6f291-111">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="6f291-111">**ResultCode**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_resultcode)         | <span data-ttu-id="6f291-112">Возвращает значение [**оператионресулткоде**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) , указывающее результат операции над обновлением.</span><span class="sxs-lookup"><span data-stu-id="6f291-112">Gets an [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) value that specifies the result of an operation on an update.</span></span>          |



 

 

 



