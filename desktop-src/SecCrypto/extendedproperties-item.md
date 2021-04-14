---
description: Свойство Item извлекает объект ExtendedProperty из коллекции. Это свойство по умолчанию.
ms.assetid: add819e1-6330-483a-8a76-3b7fb8d3f110
title: Расширенных свойств. Item, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 200e36f232c97c1b5a86c8a8a975783469d64a71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668630"
---
# <a name="extendedpropertiesitem-property"></a><span data-ttu-id="67eb8-104">Расширенных свойств. Item, свойство</span><span class="sxs-lookup"><span data-stu-id="67eb8-104">ExtendedProperties.Item property</span></span>

<span data-ttu-id="67eb8-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="67eb8-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="67eb8-106">Вместо этого используйте службы вызова платформы (PInvoke) для вызова функции Win32 API [**цертжетцертификатеконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) и получения свойств.</span><span class="sxs-lookup"><span data-stu-id="67eb8-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="67eb8-107">Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода.</span><span class="sxs-lookup"><span data-stu-id="67eb8-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="67eb8-108">[.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]</span><span class="sxs-lookup"><span data-stu-id="67eb8-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="67eb8-109">Свойство **Item** извлекает объект [**ExtendedProperty**](extendedproperty.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="67eb8-109">The **Item** property retrieves an [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span> <span data-ttu-id="67eb8-110">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="67eb8-110">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="67eb8-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67eb8-111">Syntax</span></span>


```VB
ExtendedProperties.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="67eb8-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="67eb8-112">Property value</span></span>

<span data-ttu-id="67eb8-113">Объект [**ExtendedProperty**](extendedproperty.md) , представляющий индексированное расширенное свойство коллекции.</span><span class="sxs-lookup"><span data-stu-id="67eb8-113">An [**ExtendedProperty**](extendedproperty.md) object that represents the indexed extended property of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="67eb8-114">Требования</span><span class="sxs-lookup"><span data-stu-id="67eb8-114">Requirements</span></span>



| <span data-ttu-id="67eb8-115">Требование</span><span class="sxs-lookup"><span data-stu-id="67eb8-115">Requirement</span></span> | <span data-ttu-id="67eb8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="67eb8-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67eb8-117">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="67eb8-117">End of client support</span></span><br/> | <span data-ttu-id="67eb8-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67eb8-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="67eb8-119">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="67eb8-119">End of server support</span></span><br/> | <span data-ttu-id="67eb8-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67eb8-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="67eb8-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="67eb8-121">Redistributable</span></span><br/>       | <span data-ttu-id="67eb8-122">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="67eb8-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="67eb8-123">DLL</span><span class="sxs-lookup"><span data-stu-id="67eb8-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="67eb8-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67eb8-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
