---
description: Извлекает объект EKU, представляющий свойство расширенного использования ключа (EKU).
ms.assetid: b8c12a7a-e836-48c2-958c-937b3723f85b
title: 'Свойство Иекус:: Item'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKUs.Item
- IEKUs.get_Item
- EKUs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e3eaf8d0b303207aae3ef78cc82771e1436b1027
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648907"
---
# <a name="iekusitem-property"></a><span data-ttu-id="9f9a8-103">Свойство Иекус:: Item</span><span class="sxs-lookup"><span data-stu-id="9f9a8-103">IEKUs::Item property</span></span>

<span data-ttu-id="9f9a8-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="9f9a8-105">Вместо этого используйте [**класс X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="9f9a8-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="9f9a8-106">Свойство **Item** извлекает объект [**EKU**](eku.md) , представляющий свойство расширенного использования ключа (EKU).</span><span class="sxs-lookup"><span data-stu-id="9f9a8-106">The **Item** property retrieves the [**EKU**](eku.md) object that represents the indexed extended key usage (EKU) property.</span></span>

<span data-ttu-id="9f9a8-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9f9a8-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f9a8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f9a8-108">Syntax</span></span>


```VB
EKUs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="9f9a8-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9f9a8-109">Property value</span></span>

<span data-ttu-id="9f9a8-110">Объект [**EKU**](eku.md) , представляющий свойство с индексированным расширенным использованием ключа (EKU).</span><span class="sxs-lookup"><span data-stu-id="9f9a8-110">An [**EKU**](eku.md) object that represents the indexed extended key usage (EKU) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f9a8-111">Требования</span><span class="sxs-lookup"><span data-stu-id="9f9a8-111">Requirements</span></span>



| <span data-ttu-id="9f9a8-112">Требование</span><span class="sxs-lookup"><span data-stu-id="9f9a8-112">Requirement</span></span> | <span data-ttu-id="9f9a8-113">Значение</span><span class="sxs-lookup"><span data-stu-id="9f9a8-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f9a8-114">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="9f9a8-114">End of client support</span></span><br/> | <span data-ttu-id="9f9a8-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f9a8-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9f9a8-116">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="9f9a8-116">End of server support</span></span><br/> | <span data-ttu-id="9f9a8-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f9a8-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9f9a8-118">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="9f9a8-118">Redistributable</span></span><br/>       | <span data-ttu-id="9f9a8-119">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="9f9a8-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9f9a8-120">DLL</span><span class="sxs-lookup"><span data-stu-id="9f9a8-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9f9a8-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f9a8-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f9a8-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f9a8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f9a8-123">**EKU**</span><span class="sxs-lookup"><span data-stu-id="9f9a8-123">**EKUs**</span></span>](ekus.md)
</dt> </dl>

 

 
