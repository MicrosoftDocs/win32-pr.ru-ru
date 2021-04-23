---
description: Очищает кэшированные данные пользователя объекта.
title: Дидисккуотаусер. unvalidate, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.Invalidate
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e0ffd5b7-db1d-40a4-810a-ff43549b0c9b
ms.openlocfilehash: 2b07ae6fd210b8722378a771cda97c2c04572c66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540482"
---
# <a name="didiskquotauserinvalidate-method"></a><span data-ttu-id="c1518-103">Дидисккуотаусер. unvalidate, метод</span><span class="sxs-lookup"><span data-stu-id="c1518-103">DIDiskQuotaUser.Invalidate method</span></span>

<span data-ttu-id="c1518-104">Очищает кэшированные данные пользователя объекта.</span><span class="sxs-lookup"><span data-stu-id="c1518-104">Clears the object's cached user information.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1518-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1518-105">Syntax</span></span>


```JScript
DIDiskQuotaUser.Invalidate()
```



## <a name="parameters"></a><span data-ttu-id="c1518-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1518-106">Parameters</span></span>

<span data-ttu-id="c1518-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c1518-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c1518-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1518-108">Return value</span></span>

<span data-ttu-id="c1518-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c1518-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1518-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="c1518-110">Remarks</span></span>

<span data-ttu-id="c1518-111">Этот метод очищает сведения о пользователе, хранящиеся в кэше объекта.</span><span class="sxs-lookup"><span data-stu-id="c1518-111">This method clears the user information stored in the object's cache.</span></span> <span data-ttu-id="c1518-112">При следующем запросе данных, относящихся к квотам, объект получает сведения из тома NTFS и обновляет кэш.</span><span class="sxs-lookup"><span data-stu-id="c1518-112">The next time a request is made for quota-related information, the object retrieves the information from the NTFS volume and refreshes the cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1518-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c1518-113">Requirements</span></span>



| <span data-ttu-id="c1518-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c1518-114">Requirement</span></span> | <span data-ttu-id="c1518-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c1518-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1518-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1518-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c1518-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c1518-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c1518-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1518-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c1518-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c1518-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c1518-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c1518-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1518-121"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="c1518-121"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1518-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1518-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1518-123">**Объект Дидисккуотаусер**</span><span class="sxs-lookup"><span data-stu-id="c1518-123">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




