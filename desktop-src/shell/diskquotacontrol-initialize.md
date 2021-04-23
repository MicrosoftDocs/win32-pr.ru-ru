---
description: Открывает указанный том и инициализирует его объект управления квотой.
ms.assetid: 20eae2a3-f602-48a2-bf1c-65570e7a5d21
title: DiskQuotaControl.Iniметод тиализе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.Initialize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 919720f01c67b6df3189b760aa8cefbb29615179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984248"
---
# <a name="diskquotacontrolinitialize-method"></a><span data-ttu-id="f89f8-103">DiskQuotaControl.Iniметод тиализе</span><span class="sxs-lookup"><span data-stu-id="f89f8-103">DiskQuotaControl.Initialize method</span></span>

<span data-ttu-id="f89f8-104">Открывает указанный том и инициализирует его объект управления квотой.</span><span class="sxs-lookup"><span data-stu-id="f89f8-104">Opens a specified volume and initializes its quota control object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f89f8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f89f8-105">Syntax</span></span>


```JScript
DiskQuotaControl.Initialize(
  sPath,
  bReadWrite
)
```



## <a name="parameters"></a><span data-ttu-id="f89f8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f89f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f89f8-107">*спас*</span><span class="sxs-lookup"><span data-stu-id="f89f8-107">*sPath*</span></span> 
</dt> <dd>

<span data-ttu-id="f89f8-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="f89f8-108">Type: **String**</span></span>

<span data-ttu-id="f89f8-109">Строковое значение, содержащее полный путь к тому, который должен быть инициализирован.</span><span class="sxs-lookup"><span data-stu-id="f89f8-109">A string value that contains the fully qualified path of the volume to be initialized.</span></span>

</dd> <dt>

<span data-ttu-id="f89f8-110">*бреадврите*</span><span class="sxs-lookup"><span data-stu-id="f89f8-110">*bReadWrite*</span></span> 
</dt> <dd>

<span data-ttu-id="f89f8-111">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f89f8-111">Type: **Boolean**</span></span>

<span data-ttu-id="f89f8-112">Логическое значение, указывающее способ открытия тома.</span><span class="sxs-lookup"><span data-stu-id="f89f8-112">A Boolean value that specifies how the volume is to be opened.</span></span> <span data-ttu-id="f89f8-113">Задайте для параметра *Бреадврите* **значение true** для доступа на чтение и запись или **false** для доступа только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f89f8-113">Set *bReadWrite* to **TRUE** for read/write access or **FALSE** for read-only access.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f89f8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f89f8-114">Return value</span></span>

<span data-ttu-id="f89f8-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f89f8-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f89f8-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f89f8-116">Requirements</span></span>



| <span data-ttu-id="f89f8-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f89f8-117">Requirement</span></span> | <span data-ttu-id="f89f8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f89f8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f89f8-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f89f8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f89f8-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f89f8-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f89f8-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f89f8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f89f8-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f89f8-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f89f8-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f89f8-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f89f8-124"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="f89f8-124"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f89f8-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f89f8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f89f8-126">**Объект Дисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="f89f8-126">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




