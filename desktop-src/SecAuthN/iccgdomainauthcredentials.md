---
description: Реализованный клиентом интерфейс, который позволяет разработчикам динамически предоставлять собственные учетные данные во время выполнения для проверки подлинности не присоединенных к домену контейнеров с Active Directory.
title: Интерфейс Иккгдомаинаускредентиалс (ккгплугинс. h)
ms.topic: reference
ms.date: 10/20/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- ICcgDomainAuthCredentials
api_type:
- COM
api_location:
- ccgplugins.dll
ms.openlocfilehash: 8217f806ff0a1a6b38d045c7f665758ccaf8b1f5
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387830"
---
# <a name="iccgdomainauthcredentials-interface"></a><span data-ttu-id="d1812-103">Интерфейс Иккгдомаинаускредентиалс</span><span class="sxs-lookup"><span data-stu-id="d1812-103">ICcgDomainAuthCredentials interface</span></span>

<span data-ttu-id="d1812-104">Реализованный клиентом интерфейс, который позволяет разработчикам динамически предоставлять собственные учетные данные во время выполнения для проверки подлинности не присоединенных к домену контейнеров с Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d1812-104">A client-implemented interface that allows developers to supply their own credentials dynamically at run time to authenticate non-domain joined containers with Active Directory.</span></span> 

## <a name="members"></a><span data-ttu-id="d1812-105">Участники</span><span class="sxs-lookup"><span data-stu-id="d1812-105">Members</span></span>

<span data-ttu-id="d1812-106">Интерфейс **иккгдомаинаускредентиалс** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d1812-106">The **ICcgDomainAuthCredentials** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d1812-107">**Иккгдомаинаускредентиалс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d1812-107">**ICcgDomainAuthCredentials** also has these types of members:</span></span>

-   [<span data-ttu-id="d1812-108">Методы</span><span class="sxs-lookup"><span data-stu-id="d1812-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d1812-109">Методы</span><span class="sxs-lookup"><span data-stu-id="d1812-109">Methods</span></span>

<span data-ttu-id="d1812-110">Интерфейс **иккгдомаинаускредентиалс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d1812-110">The **ICcgDomainAuthCredentials** interface has these methods.</span></span>



| <span data-ttu-id="d1812-111">Метод</span><span class="sxs-lookup"><span data-stu-id="d1812-111">Method</span></span>                                           | <span data-ttu-id="d1812-112">Описание</span><span class="sxs-lookup"><span data-stu-id="d1812-112">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1812-113">**жетпассвордкредентиалс**</span><span class="sxs-lookup"><span data-stu-id="d1812-113">**GetPasswordCredentials**</span></span>](iccgdomainauthcredentials-getpasswordcredentials.md)               | <span data-ttu-id="d1812-114">Возвращает учетные данные для проверки подлинности контейнера, не присоединенного к домену, с Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d1812-114">Returns credentials to authenticate a non-domain joined container with Active Directory.</span></span><br/>                                                              |



 

## <a name="requirements"></a><span data-ttu-id="d1812-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d1812-115">Requirements</span></span>



| <span data-ttu-id="d1812-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d1812-116">Requirement</span></span> | <span data-ttu-id="d1812-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d1812-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1812-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1812-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d1812-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d1812-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d1812-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1812-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d1812-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d1812-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d1812-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d1812-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1812-123"><dt>ккгплугинс. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1812-123"><dt>ccgplugins.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1812-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d1812-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="d1812-125"><dt>ккгплугинс. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d1812-125"><dt>ccgplugins.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d1812-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d1812-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1812-127"><dt>ccgplugins.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1812-127"><dt>ccgplugins.dll</dt></span></span> </dl> |
| <span data-ttu-id="d1812-128">IID</span><span class="sxs-lookup"><span data-stu-id="d1812-128">IID</span></span><br/>                      | <span data-ttu-id="d1812-129">6ecda518-2010-4437-8bc3-46e752b7b172</span><span class="sxs-lookup"><span data-stu-id="d1812-129">6ecda518-2010-4437-8bc3-46e752b7b172</span></span><br/>          |



 

