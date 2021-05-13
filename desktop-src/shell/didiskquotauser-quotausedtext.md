---
description: Возвращает текущий объем использования диска пользователем в виде текстовой строки.
title: Дидисккуотаусер. Куотауседтекст, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsedText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: be27a17c-77ec-4016-8c2e-16fbc88c7c7a
ms.openlocfilehash: bf818bdcd22b734c6f4638a837af97bfecef1695
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843215"
---
# <a name="didiskquotauserquotausedtext-property"></a><span data-ttu-id="4725e-103">Дидисккуотаусер. Куотауседтекст, свойство</span><span class="sxs-lookup"><span data-stu-id="4725e-103">DIDiskQuotaUser.QuotaUsedText property</span></span>

<span data-ttu-id="4725e-104">Возвращает текущий объем использования диска пользователем в виде текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="4725e-104">Gets the user's current disk usage as a text string.</span></span>

<span data-ttu-id="4725e-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4725e-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4725e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4725e-106">Syntax</span></span>


```JScript
QuotaUsedText = DIDiskQuotaUser.QuotaUsedText
```



## <a name="property-value"></a><span data-ttu-id="4725e-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4725e-107">Property value</span></span>

<span data-ttu-id="4725e-108">Строковое значение, заданное как объем используемого места на диске.</span><span class="sxs-lookup"><span data-stu-id="4725e-108">A string value that is set to the amount of disk space currently in use.</span></span> <span data-ttu-id="4725e-109">Если включено сжатие файлов NTFS, это свойство отражает объем места на диске, требуемый для данных в несжатом состоянии.</span><span class="sxs-lookup"><span data-stu-id="4725e-109">If NTFS file compression is enabled, this property reflects the amount of disk space that the data would require in an uncompressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="4725e-110">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="4725e-110">Requirements</span></span>



| <span data-ttu-id="4725e-111">Требование</span><span class="sxs-lookup"><span data-stu-id="4725e-111">Requirement</span></span> | <span data-ttu-id="4725e-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4725e-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4725e-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4725e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4725e-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4725e-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4725e-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4725e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4725e-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4725e-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4725e-117">DLL</span><span class="sxs-lookup"><span data-stu-id="4725e-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4725e-118"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="4725e-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4725e-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4725e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4725e-120">**Объект Дидисккуотаусер**</span><span class="sxs-lookup"><span data-stu-id="4725e-120">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="4725e-121">**куоталимиттекст**</span><span class="sxs-lookup"><span data-stu-id="4725e-121">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> <dt>

[<span data-ttu-id="4725e-122">**куотасрешолдтекст**</span><span class="sxs-lookup"><span data-stu-id="4725e-122">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)
</dt> <dt>

[<span data-ttu-id="4725e-123">**QuotaUsed**</span><span class="sxs-lookup"><span data-stu-id="4725e-123">**QuotaUsed**</span></span>](didiskquotauser-quotaused.md)
</dt> </dl>

 

 




