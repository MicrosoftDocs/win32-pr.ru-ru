---
description: Возвращает логическое значение, указывающее, выполняется ли перестроение файла квоты для тома.
ms.assetid: 66a6bafe-bda4-41b3-9207-2ea6b8e63835
title: Дисккуотаконтрол. Куотафилеребуилдинг, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaFileRebuilding
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e06b73e53670a136e53721b4e6bc6b2f635d601b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984412"
---
# <a name="diskquotacontrolquotafilerebuilding-property"></a><span data-ttu-id="5a0be-103">Дисккуотаконтрол. Куотафилеребуилдинг, свойство</span><span class="sxs-lookup"><span data-stu-id="5a0be-103">DiskQuotaControl.QuotaFileRebuilding property</span></span>

<span data-ttu-id="5a0be-104">Возвращает логическое значение, указывающее, выполняется ли перестроение файла квоты для тома.</span><span class="sxs-lookup"><span data-stu-id="5a0be-104">Gets a Boolean value that indicates whether the quota file for the volume is currently being rebuilt.</span></span>

<span data-ttu-id="5a0be-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5a0be-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a0be-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a0be-106">Syntax</span></span>


```JScript
bQuotaFileRebuilding = DiskQuotaControl.QuotaFileRebuilding
```



## <a name="property-value"></a><span data-ttu-id="5a0be-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5a0be-107">Property value</span></span>

<span data-ttu-id="5a0be-108">Это свойство имеет значение **true** , если выполняется перестроение файла квоты, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="5a0be-108">This property is set to **TRUE** if the quota file is being rebuilt, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a0be-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="5a0be-109">Remarks</span></span>

<span data-ttu-id="5a0be-110">Файл квоты автоматически перестраивается, когда квоты включены в системе или если одна или несколько записей пользователя помечены для удаления.</span><span class="sxs-lookup"><span data-stu-id="5a0be-110">The quota file is automatically rebuilt when quotas are enabled on the system or when one or more user entries are marked for deletion.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a0be-111">Требования</span><span class="sxs-lookup"><span data-stu-id="5a0be-111">Requirements</span></span>



| <span data-ttu-id="5a0be-112">Требование</span><span class="sxs-lookup"><span data-stu-id="5a0be-112">Requirement</span></span> | <span data-ttu-id="5a0be-113">Значение</span><span class="sxs-lookup"><span data-stu-id="5a0be-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a0be-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a0be-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5a0be-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5a0be-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5a0be-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a0be-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5a0be-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5a0be-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5a0be-118">DLL</span><span class="sxs-lookup"><span data-stu-id="5a0be-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a0be-119"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="5a0be-119"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a0be-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a0be-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a0be-121">**Объект Дисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="5a0be-121">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




