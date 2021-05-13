---
description: Возвращает предельную квоту по умолчанию в виде текстовой строки.
title: Дисккуотаконтрол. Дефаулткуоталимиттекст, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaLimitText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ea1b02e0-c480-4ef1-b6e0-1ec202d5f3c5
ms.openlocfilehash: 14a5b5a0cc42bda17f922020a8485430797875e1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841545"
---
# <a name="diskquotacontroldefaultquotalimittext-property"></a><span data-ttu-id="4a27a-103">Дисккуотаконтрол. Дефаулткуоталимиттекст, свойство</span><span class="sxs-lookup"><span data-stu-id="4a27a-103">DiskQuotaControl.DefaultQuotaLimitText property</span></span>

<span data-ttu-id="4a27a-104">Возвращает предельную квоту по умолчанию в виде текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="4a27a-104">Gets the default quota limit as a text string.</span></span>

<span data-ttu-id="4a27a-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4a27a-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a27a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a27a-106">Syntax</span></span>


```JScript
DefaultQuotaLimitText = DiskQuotaControl.DefaultQuotaLimitText
```



## <a name="property-value"></a><span data-ttu-id="4a27a-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4a27a-107">Property value</span></span>

<span data-ttu-id="4a27a-108">Строковое значение, содержащее ограничение квоты по умолчанию для новых пользователей тома.</span><span class="sxs-lookup"><span data-stu-id="4a27a-108">A string value that contains the default quota limit for new users of the volume.</span></span> <span data-ttu-id="4a27a-109">Например, если квота по умолчанию — 10,5 МБ, значение свойства равно "10,5 МБ".</span><span class="sxs-lookup"><span data-stu-id="4a27a-109">For example, if the default quota is 10.5 MB, the value of the property is "10.5 MB".</span></span> <span data-ttu-id="4a27a-110">Если у тома нет квоты по умолчанию, свойство имеет значение "без ограничений" или локализованный эквивалент.</span><span class="sxs-lookup"><span data-stu-id="4a27a-110">If the volume has no default quota, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a27a-111">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="4a27a-111">Requirements</span></span>



| <span data-ttu-id="4a27a-112">Требование</span><span class="sxs-lookup"><span data-stu-id="4a27a-112">Requirement</span></span> | <span data-ttu-id="4a27a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="4a27a-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a27a-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a27a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4a27a-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4a27a-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4a27a-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a27a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4a27a-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4a27a-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4a27a-118">DLL</span><span class="sxs-lookup"><span data-stu-id="4a27a-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a27a-119"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="4a27a-119"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a27a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a27a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a27a-121">**дефаулткуоталимит**</span><span class="sxs-lookup"><span data-stu-id="4a27a-121">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="4a27a-122">**дисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="4a27a-122">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




