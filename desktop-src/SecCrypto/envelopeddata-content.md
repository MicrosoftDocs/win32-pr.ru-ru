---
description: Задает или получает содержимое открытого текста сообщения, которое будет запечатано. Это свойство по умолчанию.
ms.assetid: 7927321f-fbda-45e0-9b9f-c10ecd3a98b1
title: Енвелопеддата. Content, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ce87dba503d8e8eec2dc21a9024c1071b3255f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648716"
---
# <a name="envelopeddatacontent-property"></a><span data-ttu-id="99745-104">Енвелопеддата. Content, свойство</span><span class="sxs-lookup"><span data-stu-id="99745-104">EnvelopedData.Content property</span></span>

<span data-ttu-id="99745-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="99745-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="99745-106">Вместо этого используйте [**класс EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="99745-106">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="99745-107">Свойство **Content** задает или получает содержимое открытого текста сообщения, которое должно быть запечатано.</span><span class="sxs-lookup"><span data-stu-id="99745-107">The **Content** property sets or retrieves the plaintext content of a message to be enveloped.</span></span> <span data-ttu-id="99745-108">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="99745-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="99745-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99745-109">Syntax</span></span>


```VB
EnvelopedData.Content As String
```



## <a name="property-value"></a><span data-ttu-id="99745-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="99745-110">Property value</span></span>

<span data-ttu-id="99745-111">Содержимое открытого текста сообщения, которое должно быть запечатано.</span><span class="sxs-lookup"><span data-stu-id="99745-111">The plaintext content of a message to be enveloped.</span></span>

## <a name="remarks"></a><span data-ttu-id="99745-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99745-112">Remarks</span></span>

<span data-ttu-id="99745-113">Задание этого свойства должно выполняться до вызова метода [**Encrypt**](envelopeddata-encrypt.md) .</span><span class="sxs-lookup"><span data-stu-id="99745-113">Setting this property must be done before the [**Encrypt**](envelopeddata-encrypt.md) method is called.</span></span> <span data-ttu-id="99745-114">Если значение этого свойства сбрасывается прямо или косвенно, все [*состояние*](../secgloss/s-gly.md) объекта сбрасывается, а все зашифрованное содержимое объекта теряется.</span><span class="sxs-lookup"><span data-stu-id="99745-114">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any encrypted content in the object is lost.</span></span>

## <a name="requirements"></a><span data-ttu-id="99745-115">Требования</span><span class="sxs-lookup"><span data-stu-id="99745-115">Requirements</span></span>



| <span data-ttu-id="99745-116">Требование</span><span class="sxs-lookup"><span data-stu-id="99745-116">Requirement</span></span> | <span data-ttu-id="99745-117">Значение</span><span class="sxs-lookup"><span data-stu-id="99745-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99745-118">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="99745-118">End of client support</span></span><br/> | <span data-ttu-id="99745-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99745-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="99745-120">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="99745-120">End of server support</span></span><br/> | <span data-ttu-id="99745-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99745-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="99745-122">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="99745-122">Redistributable</span></span><br/>       | <span data-ttu-id="99745-123">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="99745-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="99745-124">DLL</span><span class="sxs-lookup"><span data-stu-id="99745-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="99745-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99745-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99745-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99745-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99745-127">**енвелопеддата**</span><span class="sxs-lookup"><span data-stu-id="99745-127">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
