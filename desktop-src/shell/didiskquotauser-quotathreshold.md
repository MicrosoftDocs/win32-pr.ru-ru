---
description: Задает или возвращает порог предупреждения пользователя в байтах.
ms.assetid: 5289d472-d591-4604-91f9-252dd4a1b62b
title: Дидисккуотаусер. Куотасрешолд, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7ce336c84d086c4e4be369278a77e40e59474bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896882"
---
# <a name="didiskquotauserquotathreshold-property"></a><span data-ttu-id="9e0fb-103">Дидисккуотаусер. Куотасрешолд, свойство</span><span class="sxs-lookup"><span data-stu-id="9e0fb-103">DIDiskQuotaUser.QuotaThreshold property</span></span>

<span data-ttu-id="9e0fb-104">Задает или возвращает порог предупреждения пользователя в байтах.</span><span class="sxs-lookup"><span data-stu-id="9e0fb-104">Sets or gets the user's warning threshold, in bytes.</span></span>

<span data-ttu-id="9e0fb-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="9e0fb-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e0fb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e0fb-106">Syntax</span></span>


```JScript
iQuotaThreshold = DIDiskQuotaUser.QuotaThreshold
DIDiskQuotaUser.QuotaThreshold = iQuotaThreshold
```



## <a name="property-value"></a><span data-ttu-id="9e0fb-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9e0fb-107">Property value</span></span>

<span data-ttu-id="9e0fb-108">**Целочисленное** значение, указывающее или получающее порог предупреждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="9e0fb-108">An **Integer** value that specifies or receives the user's warning threshold.</span></span> <span data-ttu-id="9e0fb-109">Если использование диска пользователем превышает это значение, а свойство [**логкуотасрешолд**](diskquotacontrol-logquotathreshold.md) имеет значение **true**, система создает запись в журнале событий.</span><span class="sxs-lookup"><span data-stu-id="9e0fb-109">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e0fb-110">Требования</span><span class="sxs-lookup"><span data-stu-id="9e0fb-110">Requirements</span></span>



| <span data-ttu-id="9e0fb-111">Требование</span><span class="sxs-lookup"><span data-stu-id="9e0fb-111">Requirement</span></span> | <span data-ttu-id="9e0fb-112">Значение</span><span class="sxs-lookup"><span data-stu-id="9e0fb-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e0fb-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9e0fb-113">Minimum supported client</span></span><br/> | <span data-ttu-id="9e0fb-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9e0fb-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9e0fb-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9e0fb-115">Minimum supported server</span></span><br/> | <span data-ttu-id="9e0fb-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9e0fb-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9e0fb-117">DLL</span><span class="sxs-lookup"><span data-stu-id="9e0fb-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e0fb-118"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="9e0fb-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e0fb-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e0fb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e0fb-120">**дефаулткуотасрешолд**</span><span class="sxs-lookup"><span data-stu-id="9e0fb-120">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="9e0fb-121">**дидисккуотаусер**</span><span class="sxs-lookup"><span data-stu-id="9e0fb-121">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="9e0fb-122">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="9e0fb-122">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="9e0fb-123">**куотасрешолдтекст**</span><span class="sxs-lookup"><span data-stu-id="9e0fb-123">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)
</dt> </dl>

 

 




