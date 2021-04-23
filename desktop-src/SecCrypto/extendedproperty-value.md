---
description: Задает или получает данные расширенных свойств.
ms.assetid: 115bb52a-e64d-4d84-a491-35f6dba25a58
title: ExtendedProperty. Value, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperty.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ebbd977a107d92661110ceff02f3a5bb0bea191e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685142"
---
# <a name="extendedpropertyvalue-property"></a><span data-ttu-id="b8abb-103">ExtendedProperty. Value, свойство</span><span class="sxs-lookup"><span data-stu-id="b8abb-103">ExtendedProperty.Value property</span></span>

<span data-ttu-id="b8abb-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b8abb-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b8abb-105">Вместо этого используйте службы вызова платформы (PInvoke) для вызова функции Win32 API [**цертжетцертификатеконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) и получения свойств.</span><span class="sxs-lookup"><span data-stu-id="b8abb-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="b8abb-106">Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода.</span><span class="sxs-lookup"><span data-stu-id="b8abb-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="b8abb-107">[.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]</span><span class="sxs-lookup"><span data-stu-id="b8abb-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="b8abb-108">Свойство **value** задает или получает данные расширенного свойства.</span><span class="sxs-lookup"><span data-stu-id="b8abb-108">The **Value** property sets or retrieves the extended property data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8abb-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8abb-109">Syntax</span></span>


```VB
ExtendedProperty.Value( _
  [ ByVal EncodingType ] _
) As String
```



## <a name="property-value"></a><span data-ttu-id="b8abb-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b8abb-110">Property value</span></span>

<span data-ttu-id="b8abb-111">Данные расширенного свойства в формате, указанном параметром *енкодингтипе*.</span><span class="sxs-lookup"><span data-stu-id="b8abb-111">The extended property data, in the format specified by *EncodingType*.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8abb-112">Требования</span><span class="sxs-lookup"><span data-stu-id="b8abb-112">Requirements</span></span>



| <span data-ttu-id="b8abb-113">Требование</span><span class="sxs-lookup"><span data-stu-id="b8abb-113">Requirement</span></span> | <span data-ttu-id="b8abb-114">Значение</span><span class="sxs-lookup"><span data-stu-id="b8abb-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8abb-115">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b8abb-115">End of client support</span></span><br/> | <span data-ttu-id="b8abb-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8abb-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b8abb-117">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="b8abb-117">End of server support</span></span><br/> | <span data-ttu-id="b8abb-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8abb-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b8abb-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="b8abb-119">Redistributable</span></span><br/>       | <span data-ttu-id="b8abb-120">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="b8abb-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b8abb-121">DLL</span><span class="sxs-lookup"><span data-stu-id="b8abb-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b8abb-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8abb-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
