---
description: Возвращает пороговое значение предупреждения пользователя в виде текстовой строки.
ms.assetid: 55b53ad0-e7cd-4417-9087-297ac96e245f
title: Дидисккуотаусер. Куотасрешолдтекст, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 511829233b93dbe164ce2feccd1247ccebf3ec3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984269"
---
# <a name="didiskquotauserquotathresholdtext-property"></a><span data-ttu-id="a6742-103">Дидисккуотаусер. Куотасрешолдтекст, свойство</span><span class="sxs-lookup"><span data-stu-id="a6742-103">DIDiskQuotaUser.QuotaThresholdText property</span></span>

<span data-ttu-id="a6742-104">Возвращает пороговое значение предупреждения пользователя в виде текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="a6742-104">Gets the user's warning threshold as a text string.</span></span>

<span data-ttu-id="a6742-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a6742-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6742-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6742-106">Syntax</span></span>


```JScript
QuotaThresholdText = DIDiskQuotaUser.QuotaThresholdText
```



## <a name="property-value"></a><span data-ttu-id="a6742-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a6742-107">Property value</span></span>

<span data-ttu-id="a6742-108">Строковое значение, содержащее порог предупреждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a6742-108">The string value that contains the user's warning threshold.</span></span> <span data-ttu-id="a6742-109">Если использование диска пользователем превышает это значение, а свойство [**логкуотасрешолд**](diskquotacontrol-logquotathreshold.md) имеет значение **true**, система создает запись в журнале событий.</span><span class="sxs-lookup"><span data-stu-id="a6742-109">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6742-110">Требования</span><span class="sxs-lookup"><span data-stu-id="a6742-110">Requirements</span></span>



| <span data-ttu-id="a6742-111">Требование</span><span class="sxs-lookup"><span data-stu-id="a6742-111">Requirement</span></span> | <span data-ttu-id="a6742-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a6742-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6742-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a6742-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a6742-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a6742-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a6742-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a6742-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a6742-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a6742-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a6742-117">DLL</span><span class="sxs-lookup"><span data-stu-id="a6742-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6742-118"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="a6742-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6742-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6742-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6742-120">**Объект Идисккуотаусер**</span><span class="sxs-lookup"><span data-stu-id="a6742-120">**IDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="a6742-121">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="a6742-121">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="a6742-122">**куоталимиттекст**</span><span class="sxs-lookup"><span data-stu-id="a6742-122">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> <dt>

[<span data-ttu-id="a6742-123">**куотасрешолд**</span><span class="sxs-lookup"><span data-stu-id="a6742-123">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)
</dt> </dl>

 

 




