---
description: Задает или получает данные для подписи. Это свойство по умолчанию.
ms.assetid: 554ca500-403d-4c2a-868e-9e635d0b358e
title: Сигнеддата. Content, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3c2ac97eeee317b4ec170338f666e5b5d9277861
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669315"
---
# <a name="signeddatacontent-property"></a><span data-ttu-id="ab249-104">Сигнеддата. Content, свойство</span><span class="sxs-lookup"><span data-stu-id="ab249-104">SignedData.Content property</span></span>

<span data-ttu-id="ab249-105">\[Свойство **Content** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="ab249-105">\[The **Content** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ab249-106">Вместо этого используйте [**класс SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="ab249-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="ab249-107">Свойство **Content** задает или получает данные для подписи.</span><span class="sxs-lookup"><span data-stu-id="ab249-107">The **Content** property sets or retrieves the data to be signed.</span></span> <span data-ttu-id="ab249-108">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ab249-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab249-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab249-109">Syntax</span></span>


```VB
SignedData.Content As String
```



## <a name="property-value"></a><span data-ttu-id="ab249-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ab249-110">Property value</span></span>

<span data-ttu-id="ab249-111">Данные, которые должны быть подписаны.</span><span class="sxs-lookup"><span data-stu-id="ab249-111">The data to be signed.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab249-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ab249-112">Remarks</span></span>

<span data-ttu-id="ab249-113">Это свойство должно быть инициализировано до вызова метода [**Sign**](signeddata-sign.md) .</span><span class="sxs-lookup"><span data-stu-id="ab249-113">This property must be initialized before the [**Sign**](signeddata-sign.md) method is called.</span></span> <span data-ttu-id="ab249-114">Когда значение этого свойства сбрасывается прямо или косвенно, все [*состояние*](../secgloss/s-gly.md) объекта сбрасывается, и все сигнатуры, связанные с объектом до изменения свойства, теряются.</span><span class="sxs-lookup"><span data-stu-id="ab249-114">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any signature that was associated with the object before the property was changed is lost.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab249-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ab249-115">Requirements</span></span>



| <span data-ttu-id="ab249-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ab249-116">Requirement</span></span> | <span data-ttu-id="ab249-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ab249-117">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab249-118">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="ab249-118">Redistributable</span></span><br/> | <span data-ttu-id="ab249-119">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="ab249-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ab249-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ab249-120">DLL</span></span><br/>             | <dl> <span data-ttu-id="ab249-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab249-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab249-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab249-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab249-123">**сигнеддата**</span><span class="sxs-lookup"><span data-stu-id="ab249-123">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
