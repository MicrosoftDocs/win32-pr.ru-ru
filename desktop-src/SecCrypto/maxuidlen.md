---
description: Числовая константа, указывающая максимальное число символов, которые будут использоваться некоторыми поставщиками служб шифрования Майкрософт при получении идентификатора пользователя.
ms.assetid: cc15a166-9a0c-41ce-9cb1-ecdc922565c0
title: МАКСУИДЛЕН (Винкрипт. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 199d8e697deba86ffe48d4f76501f2d9d3a6d4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682778"
---
# <a name="maxuidlen"></a><span data-ttu-id="50143-103">максуидлен</span><span class="sxs-lookup"><span data-stu-id="50143-103">MAXUIDLEN</span></span>

<span data-ttu-id="50143-104">МАКСУИДЛЕН — это числовая константа, указывающая максимальное число символов, которые будут использоваться некоторыми поставщиками служб шифрования Майкрософт при получении идентификатора пользователя. МАКСУИДЛЕН определяется в Винкрипт. h.</span><span class="sxs-lookup"><span data-stu-id="50143-104">MAXUIDLEN is a numeric constant that specifies the maximum number of characters that some of the Microsoft cryptographic providers will use when obtaining the user ID.MAXUIDLEN is defined in Wincrypt.h.</span></span>



| <span data-ttu-id="50143-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="50143-105">Constant/value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="50143-106">Описание</span><span class="sxs-lookup"><span data-stu-id="50143-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MAXUIDLEN"></span><span id="maxuidlen"></span><dl> <span data-ttu-id="50143-107"><dt>**Максуидлен**</dt> <dt>64 (0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="50143-107"><dt>**MAXUIDLEN**</dt> <dt>64 (0x40)</dt></span></span> </dl> | <span data-ttu-id="50143-108">Если параметр *псзконтаинер* функции [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) имеет **значение NULL**, некоторые поставщики служб шифрования Майкрософт используют имя входа пользователя, вошедшего в систему, в качестве имени контейнера ключей.</span><span class="sxs-lookup"><span data-stu-id="50143-108">When the *pszContainer* parameter of the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function is **NULL**, some of the Microsoft cryptographic providers use the logon name of the currently logged on user as the key container name.</span></span> <span data-ttu-id="50143-109">МАКСУИДЛЕН указывает максимальное число символов, включая завершающий символ **null** , который эти поставщики будут использовать для имени пользователя.</span><span class="sxs-lookup"><span data-stu-id="50143-109">MAXUIDLEN specifies the maximum number of characters, including the terminating **NULL** character, that these providers will use for the user name.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="50143-110">Требования</span><span class="sxs-lookup"><span data-stu-id="50143-110">Requirements</span></span>



| <span data-ttu-id="50143-111">Требование</span><span class="sxs-lookup"><span data-stu-id="50143-111">Requirement</span></span> | <span data-ttu-id="50143-112">Значение</span><span class="sxs-lookup"><span data-stu-id="50143-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50143-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50143-113">Minimum supported client</span></span><br/> | <span data-ttu-id="50143-114">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="50143-114">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="50143-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50143-115">Minimum supported server</span></span><br/> | <span data-ttu-id="50143-116">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="50143-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="50143-117">Header</span><span class="sxs-lookup"><span data-stu-id="50143-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="50143-118"><dt>Винкрипт. h</dt></span><span class="sxs-lookup"><span data-stu-id="50143-118"><dt>Wincrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50143-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50143-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50143-120">**CryptAcquireContext**</span><span class="sxs-lookup"><span data-stu-id="50143-120">**CryptAcquireContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)
</dt> <dt>

[<span data-ttu-id="50143-121">**кпаккуиреконтекст**</span><span class="sxs-lookup"><span data-stu-id="50143-121">**CPAcquireContext**</span></span>](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> </dl>

 

 




