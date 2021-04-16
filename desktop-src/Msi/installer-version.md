---
description: Свойство Version объекта Installer является свойством только для чтения, которое является строковым представлением текущей версии установщик Windows. Строка возвращается в следующей форме.
ms.assetid: 9af262f0-b573-471d-aac6-6a72e8cb5314
title: Свойство установщика. Version
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Version
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 29af85b8fc1afe468dc87d5516da9a528024c73a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652157"
---
# <a name="installerversion-property"></a><span data-ttu-id="720de-104">Свойство установщика. Version</span><span class="sxs-lookup"><span data-stu-id="720de-104">Installer.Version property</span></span>

<span data-ttu-id="720de-105">Свойство **Version** объекта [**Installer**](installer-object.md) является свойством только для чтения, которое является строковым представлением текущей версии установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="720de-105">The **Version** property of the [**Installer**](installer-object.md) object is a read-only property that is the string representation of the current version of Windows Installer.</span></span> <span data-ttu-id="720de-106">Строка возвращается в следующей форме.</span><span class="sxs-lookup"><span data-stu-id="720de-106">The string is returned in the following form.</span></span>

<span data-ttu-id="720de-107">*основной*. *дополнительный номер*. *Сборка*. *Обновление*</span><span class="sxs-lookup"><span data-stu-id="720de-107">*major*.*minor*.*build*.*update*</span></span>

<span data-ttu-id="720de-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="720de-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="720de-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="720de-109">Syntax</span></span>


```JScript
propVal = Installer.Version
```



## <a name="property-value"></a><span data-ttu-id="720de-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="720de-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="720de-111">Требования</span><span class="sxs-lookup"><span data-stu-id="720de-111">Requirements</span></span>



| <span data-ttu-id="720de-112">Требование</span><span class="sxs-lookup"><span data-stu-id="720de-112">Requirement</span></span> | <span data-ttu-id="720de-113">Значение</span><span class="sxs-lookup"><span data-stu-id="720de-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="720de-114">Версия</span><span class="sxs-lookup"><span data-stu-id="720de-114">Version</span></span><br/> | <span data-ttu-id="720de-115">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="720de-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="720de-116">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="720de-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="720de-117">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="720de-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="720de-118">DLL</span><span class="sxs-lookup"><span data-stu-id="720de-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="720de-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="720de-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="720de-120">IID</span><span class="sxs-lookup"><span data-stu-id="720de-120">IID</span></span><br/>     | <span data-ttu-id="720de-121">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="720de-121">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




