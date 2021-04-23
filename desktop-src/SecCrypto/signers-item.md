---
description: Извлекает объект подписавший, представляющий индексированный подписывающий.
ms.assetid: a95f4e33-ab92-44e1-91ab-2c5335a04f05
title: Свойство Signs. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9b0b4179c1ea7e2ded5d945f64f03124eb864fdc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689476"
---
# <a name="signersitem-property"></a><span data-ttu-id="6d552-103">Свойство Signs. Item</span><span class="sxs-lookup"><span data-stu-id="6d552-103">Signers.Item property</span></span>

<span data-ttu-id="6d552-104">\[Свойство **Item** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="6d552-104">\[The **Item** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6d552-105">Вместо этого используйте коллекцию объектов Кмссигнер.</span><span class="sxs-lookup"><span data-stu-id="6d552-105">Instead, use a collection of CmsSigner objects.</span></span> <span data-ttu-id="6d552-106">Дополнительные сведения см. в описании [**класса кмссигнер**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="6d552-106">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="6d552-107">Свойство **Item** получает объект [**подписавший**](signer.md) , представляющий индексированный подписывающий.</span><span class="sxs-lookup"><span data-stu-id="6d552-107">The **Item** property retrieves the [**Signer**](signer.md) object that represents the indexed signer.</span></span> <span data-ttu-id="6d552-108">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6d552-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d552-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d552-109">Syntax</span></span>


```VB
Signers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="6d552-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6d552-110">Property value</span></span>

<span data-ttu-id="6d552-111">Объект [**SignIn**](signer.md) , представляющий индексированный подписывающий.</span><span class="sxs-lookup"><span data-stu-id="6d552-111">The [**Signer**](signer.md) object that represents the indexed signer.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d552-112">Требования</span><span class="sxs-lookup"><span data-stu-id="6d552-112">Requirements</span></span>



| <span data-ttu-id="6d552-113">Требование</span><span class="sxs-lookup"><span data-stu-id="6d552-113">Requirement</span></span> | <span data-ttu-id="6d552-114">Значение</span><span class="sxs-lookup"><span data-stu-id="6d552-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d552-115">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="6d552-115">Redistributable</span></span><br/> | <span data-ttu-id="6d552-116">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="6d552-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6d552-117">DLL</span><span class="sxs-lookup"><span data-stu-id="6d552-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="6d552-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d552-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d552-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d552-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d552-120">**Подписавшими**</span><span class="sxs-lookup"><span data-stu-id="6d552-120">**Signers**</span></span>](signers.md)
</dt> </dl>

 

 
