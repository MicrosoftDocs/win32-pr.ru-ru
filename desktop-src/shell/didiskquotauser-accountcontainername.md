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
ms.openlocfilehash: ef96b296d77979e5ef72c2804ad24628f0b0d8f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808819"
---
# <a name="didiskquotauseraccountcontainername-property"></a><span data-ttu-id="70a5f-103">Дидисккуотаусер. Аккаунтконтаинернаме, свойство</span><span class="sxs-lookup"><span data-stu-id="70a5f-103">DIDiskQuotaUser.AccountContainerName property</span></span>

<span data-ttu-id="70a5f-104">Возвращает имя контейнера учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="70a5f-104">Gets the name of the user's account container.</span></span>

<span data-ttu-id="70a5f-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="70a5f-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="70a5f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70a5f-106">Syntax</span></span>


```JScript
AccountContainerName = DIDiskQuotaUser.AccountContainerName
```



## <a name="property-value"></a><span data-ttu-id="70a5f-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="70a5f-107">Property value</span></span>

<span data-ttu-id="70a5f-108">Строковое значение, заданное для имени контейнера учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="70a5f-108">A string value that is set to the user's account container name.</span></span>

## <a name="remarks"></a><span data-ttu-id="70a5f-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="70a5f-109">Remarks</span></span>

<span data-ttu-id="70a5f-110">Для учетных записей без сведений о службах каталогов это свойство содержит имя домена.</span><span class="sxs-lookup"><span data-stu-id="70a5f-110">For accounts without directory services information, this property contains the domain name.</span></span> <span data-ttu-id="70a5f-111">Для учетных записей со сведениями о службах каталогов это свойство содержит каноническое имя с удаленным именем завершающего объекта.</span><span class="sxs-lookup"><span data-stu-id="70a5f-111">For accounts with directory services information, this property contains a canonical name with the terminating object name removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="70a5f-112">Требования</span><span class="sxs-lookup"><span data-stu-id="70a5f-112">Requirements</span></span>



| <span data-ttu-id="70a5f-113">Требование</span><span class="sxs-lookup"><span data-stu-id="70a5f-113">Requirement</span></span> | <span data-ttu-id="70a5f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="70a5f-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70a5f-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70a5f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="70a5f-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="70a5f-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="70a5f-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70a5f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="70a5f-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="70a5f-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="70a5f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="70a5f-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70a5f-120"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="70a5f-120"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70a5f-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70a5f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70a5f-122">**Объект Дидисккуотаусер**</span><span class="sxs-lookup"><span data-stu-id="70a5f-122">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




