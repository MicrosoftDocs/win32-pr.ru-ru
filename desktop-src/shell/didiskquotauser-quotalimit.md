---
description: Задает или возвращает текущую квоту пользователя.
title: Дидисккуотаусер. QuotaLimit, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 7eee1be7-8ad5-4796-910c-987fe3fd6338
ms.openlocfilehash: 6c13c0d38c3c5f4387b7ee90165057edb111124a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984272"
---
# <a name="didiskquotauserquotalimit-property"></a><span data-ttu-id="1e6d1-103">Дидисккуотаусер. QuotaLimit, свойство</span><span class="sxs-lookup"><span data-stu-id="1e6d1-103">DIDiskQuotaUser.QuotaLimit property</span></span>

<span data-ttu-id="1e6d1-104">Задает или возвращает текущую [**квоту**](diskquotacontrol-object.md)пользователя.</span><span class="sxs-lookup"><span data-stu-id="1e6d1-104">Sets or gets the user's current [**quota limit**](diskquotacontrol-object.md).</span></span>

<span data-ttu-id="1e6d1-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1e6d1-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e6d1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e6d1-106">Syntax</span></span>


```JScript
iQuotaLimit = DIDiskQuotaUser.QuotaLimit
DIDiskQuotaUser.QuotaLimit = iQuotaLimit
```



## <a name="property-value"></a><span data-ttu-id="1e6d1-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1e6d1-107">Property value</span></span>

<span data-ttu-id="1e6d1-108">**Целочисленное** значение, которое указывает или получает текущее ограничение квоты пользователя в байтах.</span><span class="sxs-lookup"><span data-stu-id="1e6d1-108">An **Integer** value that specifies or receives the user's current quota limit, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e6d1-109">Требования</span><span class="sxs-lookup"><span data-stu-id="1e6d1-109">Requirements</span></span>



| <span data-ttu-id="1e6d1-110">Требование</span><span class="sxs-lookup"><span data-stu-id="1e6d1-110">Requirement</span></span> | <span data-ttu-id="1e6d1-111">Значение</span><span class="sxs-lookup"><span data-stu-id="1e6d1-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e6d1-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e6d1-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1e6d1-113">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1e6d1-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e6d1-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e6d1-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1e6d1-115">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1e6d1-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1e6d1-116">DLL</span><span class="sxs-lookup"><span data-stu-id="1e6d1-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e6d1-117"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="1e6d1-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e6d1-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e6d1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e6d1-119">**дефаулткуоталимит**</span><span class="sxs-lookup"><span data-stu-id="1e6d1-119">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="1e6d1-120">**дидисккуотаусер**</span><span class="sxs-lookup"><span data-stu-id="1e6d1-120">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="1e6d1-121">**куоталимиттекст**</span><span class="sxs-lookup"><span data-stu-id="1e6d1-121">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> </dl>

 

 




