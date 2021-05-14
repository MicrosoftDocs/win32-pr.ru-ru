---
description: Возвращает текущее использование диска пользователем в байтах.
title: Дидисккуотаусер. Куотаусед, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsed
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3e3ade59-b925-4ff5-ae7e-ed97eff506c7
ms.openlocfilehash: a08d7579ad4de51fbc88b7091f2f906ace838883
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841575"
---
# <a name="didiskquotauserquotaused-property"></a><span data-ttu-id="a66b1-103">Дидисккуотаусер. Куотаусед, свойство</span><span class="sxs-lookup"><span data-stu-id="a66b1-103">DIDiskQuotaUser.QuotaUsed property</span></span>

<span data-ttu-id="a66b1-104">Возвращает текущее использование диска пользователем в байтах.</span><span class="sxs-lookup"><span data-stu-id="a66b1-104">Gets the user's current disk usage, in bytes.</span></span>

<span data-ttu-id="a66b1-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a66b1-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a66b1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a66b1-106">Syntax</span></span>


```JScript
iQuotaUsed = DIDiskQuotaUser.QuotaUsed
```



## <a name="property-value"></a><span data-ttu-id="a66b1-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a66b1-107">Property value</span></span>

<span data-ttu-id="a66b1-108">**Целочисленное** значение, которое задается как количество места на диске, используемое в данный момент.</span><span class="sxs-lookup"><span data-stu-id="a66b1-108">The **Integer** value that is set to the amount of disk space currently in use.</span></span> <span data-ttu-id="a66b1-109">Если включено сжатие файлов NTFS, **куотаусед** отражает объем дискового пространства, требуемого для данных в несжатом состоянии.</span><span class="sxs-lookup"><span data-stu-id="a66b1-109">If NTFS file compression is enabled, **QuotaUsed** reflects the amount of disk space that the data would require in an uncompressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="a66b1-110">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="a66b1-110">Requirements</span></span>



| <span data-ttu-id="a66b1-111">Требование</span><span class="sxs-lookup"><span data-stu-id="a66b1-111">Requirement</span></span> | <span data-ttu-id="a66b1-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a66b1-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a66b1-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a66b1-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a66b1-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a66b1-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a66b1-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a66b1-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a66b1-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a66b1-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a66b1-117">DLL</span><span class="sxs-lookup"><span data-stu-id="a66b1-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a66b1-118"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="a66b1-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a66b1-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a66b1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a66b1-120">**дидисккуотаусер**</span><span class="sxs-lookup"><span data-stu-id="a66b1-120">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="a66b1-121">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="a66b1-121">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="a66b1-122">**куотасрешолд**</span><span class="sxs-lookup"><span data-stu-id="a66b1-122">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)
</dt> <dt>

[<span data-ttu-id="a66b1-123">**куотауседтекст**</span><span class="sxs-lookup"><span data-stu-id="a66b1-123">**QuotaUsedText**</span></span>](didiskquotauser-quotausedtext.md)
</dt> </dl>

 

 




