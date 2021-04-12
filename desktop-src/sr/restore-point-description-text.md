---
title: Текст описания точки восстановления
description: Когда приложение вызывает функцию Срсетресторепоинт, оно может предоставить любой текст в качестве описания для точки восстановления. Однако в следующей таблице показан рекомендуемый текст описания.
ms.assetid: e6e1974b-c162-4019-9349-936f3786cb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e90fd1b7d5776c8c3798a68946382cc702b3bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258517"
---
# <a name="restore-point-description-text"></a><span data-ttu-id="054c4-103">Текст описания точки восстановления</span><span class="sxs-lookup"><span data-stu-id="054c4-103">Restore Point Description Text</span></span>

<span data-ttu-id="054c4-104">Когда приложение вызывает функцию [**срсетресторепоинт**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) , оно может предоставить любой текст в качестве описания для точки восстановления. Однако в следующей таблице показан рекомендуемый текст описания.</span><span class="sxs-lookup"><span data-stu-id="054c4-104">When an application calls the [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) function, it can provide any text as a description for the restore point; however, the following table shows the recommended description text.</span></span>



| <span data-ttu-id="054c4-105">Изменение системы</span><span class="sxs-lookup"><span data-stu-id="054c4-105">System modification</span></span>                            | <span data-ttu-id="054c4-106">Тип точки восстановления</span><span class="sxs-lookup"><span data-stu-id="054c4-106">Restore point type</span></span>      | <span data-ttu-id="054c4-107">Описание</span><span class="sxs-lookup"><span data-stu-id="054c4-107">Description</span></span>            |
|------------------------------------------------|-------------------------|------------------------|
| <span data-ttu-id="054c4-108">Установка приложения</span><span class="sxs-lookup"><span data-stu-id="054c4-108">Application installation</span></span>                       | <span data-ttu-id="054c4-109">\_Установка приложения</span><span class="sxs-lookup"><span data-stu-id="054c4-109">APPLICATION\_INSTALL</span></span>    | <span data-ttu-id="054c4-110">Установленное *AppName*</span><span class="sxs-lookup"><span data-stu-id="054c4-110">Installed *AppName*</span></span>    |
| <span data-ttu-id="054c4-111">Изменение приложения (Добавление и удаление компонентов)</span><span class="sxs-lookup"><span data-stu-id="054c4-111">Application modification (add/remove features)</span></span> | <span data-ttu-id="054c4-112">ИЗМЕНИТЬ \_ Параметры</span><span class="sxs-lookup"><span data-stu-id="054c4-112">MODIFY\_SETTINGS</span></span>        | <span data-ttu-id="054c4-113">Настроено *AppName*</span><span class="sxs-lookup"><span data-stu-id="054c4-113">Configured *AppName*</span></span>   |
| <span data-ttu-id="054c4-114">Удаление приложения</span><span class="sxs-lookup"><span data-stu-id="054c4-114">Application removal</span></span>                            | <span data-ttu-id="054c4-115">\_Удаление приложения</span><span class="sxs-lookup"><span data-stu-id="054c4-115">APPLICATION\_UNINSTALL</span></span>  | <span data-ttu-id="054c4-116">Удалено *AppName*</span><span class="sxs-lookup"><span data-stu-id="054c4-116">Removed *AppName*</span></span>      |
| <span data-ttu-id="054c4-117">Установка драйвера устройства</span><span class="sxs-lookup"><span data-stu-id="054c4-117">Device driver installation</span></span>                     | <span data-ttu-id="054c4-118">\_Установка драйвера \_ устройства</span><span class="sxs-lookup"><span data-stu-id="054c4-118">DEVICE\_DRIVER\_INSTALL</span></span> | <span data-ttu-id="054c4-119">Установленный *имя_драйвера*</span><span class="sxs-lookup"><span data-stu-id="054c4-119">Installed *DriverName*</span></span> |



 

<span data-ttu-id="054c4-120">Установщики, такие как установщик Windows и InstallShield, используют следующие соглашения для текста описания:</span><span class="sxs-lookup"><span data-stu-id="054c4-120">Installers, such as Windows Installer and InstallShield, use these conventions for the description text:</span></span>

-   <span data-ttu-id="054c4-121">Название продукта соответствует команде. Например, установлено *AppName*.</span><span class="sxs-lookup"><span data-stu-id="054c4-121">The product name follows the verb; for example, Installed *AppName*.</span></span>
-   <span data-ttu-id="054c4-122">Имя продукта можно использовать отдельно (*AppName*), а название продукта и название компании могут быть использованы (*MyCompany AppName*).</span><span class="sxs-lookup"><span data-stu-id="054c4-122">The product name can be used alone (*AppName*) or the product name and the company name may both be used (*MyCompany AppName*).</span></span>

 

 




