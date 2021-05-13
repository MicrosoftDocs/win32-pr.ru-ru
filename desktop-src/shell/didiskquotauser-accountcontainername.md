---
description: Возвращает имя контейнера учетной записи пользователя.
title: Дидисккуотаусер. Аккаунтконтаинернаме, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountContainerName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b9b0355-ea69-4c34-b0be-fc8e5855ec73
ms.openlocfilehash: 1cb709ccc4fa0afcb56314bd097b1b0120b8b59a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843355"
---
# <a name="didiskquotauseraccountcontainername-property"></a><span data-ttu-id="a7e04-103">Дидисккуотаусер. Аккаунтконтаинернаме, свойство</span><span class="sxs-lookup"><span data-stu-id="a7e04-103">DIDiskQuotaUser.AccountContainerName property</span></span>

<span data-ttu-id="a7e04-104">Возвращает имя контейнера учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="a7e04-104">Gets the name of the user's account container.</span></span>

<span data-ttu-id="a7e04-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a7e04-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7e04-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7e04-106">Syntax</span></span>


```JScript
AccountContainerName = DIDiskQuotaUser.AccountContainerName
```



## <a name="property-value"></a><span data-ttu-id="a7e04-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a7e04-107">Property value</span></span>

<span data-ttu-id="a7e04-108">Строковое значение, заданное для имени контейнера учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="a7e04-108">A string value that is set to the user's account container name.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7e04-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="a7e04-109">Remarks</span></span>

<span data-ttu-id="a7e04-110">Для учетных записей без сведений о службах каталогов это свойство содержит имя домена.</span><span class="sxs-lookup"><span data-stu-id="a7e04-110">For accounts without directory services information, this property contains the domain name.</span></span> <span data-ttu-id="a7e04-111">Для учетных записей со сведениями о службах каталогов это свойство содержит каноническое имя с удаленным именем завершающего объекта.</span><span class="sxs-lookup"><span data-stu-id="a7e04-111">For accounts with directory services information, this property contains a canonical name with the terminating object name removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7e04-112">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="a7e04-112">Requirements</span></span>



| <span data-ttu-id="a7e04-113">Требование</span><span class="sxs-lookup"><span data-stu-id="a7e04-113">Requirement</span></span> | <span data-ttu-id="a7e04-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a7e04-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e04-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7e04-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a7e04-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a7e04-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a7e04-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7e04-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a7e04-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a7e04-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a7e04-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a7e04-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7e04-120"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="a7e04-120"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7e04-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7e04-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7e04-122">**Объект Дидисккуотаусер**</span><span class="sxs-lookup"><span data-stu-id="a7e04-122">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




