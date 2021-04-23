---
title: add urlacl
description: Резервирует указанный URL-адрес для пользователей и учетных записей без прав администратора.
ms.assetid: 5d89dec3-26e6-4db8-b4cc-e9b933ac60c5
keywords:
- Добавить urlacl HTTP
topic_type:
- apiref
api_name:
- add urlacl
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 16f6cb64c0c784f3a5400e2c97e212edbc50936c
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "104000297"
---
# <a name="add-urlacl"></a><span data-ttu-id="1f52e-104">add urlacl</span><span class="sxs-lookup"><span data-stu-id="1f52e-104">add urlacl</span></span>

<span data-ttu-id="1f52e-105">Резервирует указанный URL-адрес для пользователей и учетных записей без прав администратора.</span><span class="sxs-lookup"><span data-stu-id="1f52e-105">Reserves the specified URL for non-administrator users and accounts.</span></span> <span data-ttu-id="1f52e-106">Список управления доступом на уровне пользователей (DACL) можно указать с помощью имени учетной записи с параметрами Listen и Delegate либо с помощью строки на языке определения дескрипторов безопасности (SDDL).</span><span class="sxs-lookup"><span data-stu-id="1f52e-106">The discretionary access control list (DACL) can be specified by using an account name with the listen and delegate parameters or by using a security descriptor definition language (SDDL) string.</span></span>

``` syntax
add urlacl [url=]string
           [[user=]string
           {[[listen={yes|no}] [delegate={yes|no}]] | [sddl=]string}

 
```

## <a name="parameters"></a><span data-ttu-id="1f52e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f52e-107">Parameters</span></span>

<dl> <span data-ttu-id="1f52e-108"><dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[URL =] строка**
</dt> </span><span class="sxs-lookup"><span data-stu-id="1f52e-108"><dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[url=] string**
</dt> </span></span><dd>

<span data-ttu-id="1f52e-109">Указывает полный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="1f52e-109">Specifies the fully qualified URL.</span></span>

<span data-ttu-id="1f52e-110"></dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[USER =] строка**
</dt> </span><span class="sxs-lookup"><span data-stu-id="1f52e-110"></dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[user=] string**
</dt> </span></span><dd>

<span data-ttu-id="1f52e-111">Указывает имя пользователя или группы пользователей.</span><span class="sxs-lookup"><span data-stu-id="1f52e-111">Specifies the user or user group name.</span></span>

</dd> <dt>

<span data-ttu-id="1f52e-112"><span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[Listen = {да \| нет}\]**</span><span class="sxs-lookup"><span data-stu-id="1f52e-112"><span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[listen={yes\|no}\]**</span></span>
</dt> <dd>

<span data-ttu-id="1f52e-113">Задает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="1f52e-113">Specifies one of the following values:</span></span>

-   <span data-ttu-id="1f52e-114">Да. разрешает пользователю регистрировать URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="1f52e-114">yes: Allows the user to register URLs.</span></span> <span data-ttu-id="1f52e-115">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1f52e-115">This is the default value.</span></span>
-   <span data-ttu-id="1f52e-116">Нет: запрещает пользователю регистрировать URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="1f52e-116">no: Denies the user from registering URLs.</span></span>

</dd> <dt>

<span data-ttu-id="1f52e-117"><span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[Delegate = {да \| нет}\]**</span><span class="sxs-lookup"><span data-stu-id="1f52e-117"><span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[delegate={yes\|no}\]**</span></span>
</dt> <dd>

<span data-ttu-id="1f52e-118">Задает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="1f52e-118">Specifies one of the following values:</span></span>

-   <span data-ttu-id="1f52e-119">Да. разрешает пользователю делегировать URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="1f52e-119">yes: Allows the user to delegate URLs.</span></span>
-   <span data-ttu-id="1f52e-120">Нет: запрещает пользователю делегировать URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="1f52e-120">no: Denies the user from delegating URLs.</span></span> <span data-ttu-id="1f52e-121">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1f52e-121">This is the default value.</span></span>

<span data-ttu-id="1f52e-122"></dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[SDDL =] строка**
</dt> </span><span class="sxs-lookup"><span data-stu-id="1f52e-122"></dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[sddl=] string**
</dt> </span></span><dd>

<span data-ttu-id="1f52e-123">Указывает строку SDDL, описывающую DACL.</span><span class="sxs-lookup"><span data-stu-id="1f52e-123">Specifies the SDDL string that describes the DACL.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="1f52e-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="1f52e-124">Examples</span></span>

* <span data-ttu-id="1f52e-125">add urlacl url=https://+:80/MyUri user=DOMAIN\\ user</span><span class="sxs-lookup"><span data-stu-id="1f52e-125">add urlacl url=https://+:80/MyUri user=DOMAIN\\user</span></span>

* <span data-ttu-id="1f52e-126">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes</span><span class="sxs-lookup"><span data-stu-id="1f52e-126">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes</span></span>

* <span data-ttu-id="1f52e-127">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no</span><span class="sxs-lookup"><span data-stu-id="1f52e-127">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no</span></span>

 
## <a name="see-also"></a><span data-ttu-id="1f52e-128">См. также:</span><span class="sxs-lookup"><span data-stu-id="1f52e-128">See Also</span></span>

* [<span data-ttu-id="1f52e-129">Команды HTTP для Netsh</span><span class="sxs-lookup"><span data-stu-id="1f52e-129">Netsh http commands</span></span>](/windows-server/networking/technologies/netsh/netsh-http#add-urlacl)
 