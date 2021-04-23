---
description: Задает или возвращает пороговое значение квоты по умолчанию.
ms.assetid: d3f23e52-586f-4cb8-b91c-44a71f8f94b2
title: Дисккуотаконтрол. Дефаулткуотасрешолд, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a4ce4205ee8bcc73c78bd1aabe7d8659ac3f5489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984257"
---
# <a name="diskquotacontroldefaultquotathreshold-property"></a><span data-ttu-id="e1690-103">Дисккуотаконтрол. Дефаулткуотасрешолд, свойство</span><span class="sxs-lookup"><span data-stu-id="e1690-103">DiskQuotaControl.DefaultQuotaThreshold property</span></span>

<span data-ttu-id="e1690-104">Задает или возвращает пороговое значение квоты по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e1690-104">Sets or gets the default quota threshold.</span></span>

<span data-ttu-id="e1690-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e1690-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1690-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1690-106">Syntax</span></span>


```JScript
iDefaultQuotaThreshold = DiskQuotaControl.DefaultQuotaThreshold
DiskQuotaControl.DefaultQuotaThreshold = iDefaultQuotaThreshold
```



## <a name="property-value"></a><span data-ttu-id="e1690-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e1690-107">Property value</span></span>

<span data-ttu-id="e1690-108">**Целочисленное** значение, заданное по умолчанию для порога предупреждения для новых пользователей в байтах.</span><span class="sxs-lookup"><span data-stu-id="e1690-108">An **Integer** value that is set to the default warning threshold for new users, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1690-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="e1690-109">Remarks</span></span>

<span data-ttu-id="e1690-110">Пороговое значение квоты по умолчанию применяется автоматически к новым пользователям тома.</span><span class="sxs-lookup"><span data-stu-id="e1690-110">The default quota threshold is applied automatically to new users of the volume.</span></span> <span data-ttu-id="e1690-111">Если использование диска пользователем превышает это значение, а свойство [**логкуотасрешолд**](diskquotacontrol-logquotathreshold.md) имеет значение **true**, система создает запись в журнале событий.</span><span class="sxs-lookup"><span data-stu-id="e1690-111">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span> <span data-ttu-id="e1690-112">Например, если пороговое значение по умолчанию — 10,0 МБ, значение свойства равно "10,0 МБ".</span><span class="sxs-lookup"><span data-stu-id="e1690-112">For example, if the default threshold is 10.0 MB, the value of the property is "10.0 MB".</span></span> <span data-ttu-id="e1690-113">Если для тома не задано пороговое значение по умолчанию, свойство имеет значение "без ограничений" или локализованный эквивалент.</span><span class="sxs-lookup"><span data-stu-id="e1690-113">If the volume has no default threshold, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1690-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e1690-114">Requirements</span></span>



| <span data-ttu-id="e1690-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e1690-115">Requirement</span></span> | <span data-ttu-id="e1690-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e1690-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1690-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e1690-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e1690-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e1690-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e1690-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e1690-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e1690-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e1690-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e1690-121">DLL</span><span class="sxs-lookup"><span data-stu-id="e1690-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1690-122"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="e1690-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1690-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1690-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1690-124">**дисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="e1690-124">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




