---
description: '\_Свойство NewEnum объекта расширенных свойств Извлекает интерфейс IEnumVARIANT для объекта, который можно использовать для перечисления коллекции. Это свойство скрыто в Visual Basic Scripting Edition (VBScript).'
ms.assetid: 2692f607-3bec-4674-9d8d-3c872d523ace
title: ExtendedProperties._NewEnum, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 62f07fe7a1a193f93fc0d3bf4c04fbfc5d76ecf9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668629"
---
# <a name="extendedproperties_newenum-property"></a><span data-ttu-id="fdfde-104">Расширенных свойств. \_ Свойство NewEnum</span><span class="sxs-lookup"><span data-stu-id="fdfde-104">ExtendedProperties.\_NewEnum property</span></span>

<span data-ttu-id="fdfde-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fdfde-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="fdfde-106">Вместо этого используйте службы вызова платформы (PInvoke) для вызова функции Win32 API [**цертжетцертификатеконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) и получения свойств.</span><span class="sxs-lookup"><span data-stu-id="fdfde-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="fdfde-107">Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода.</span><span class="sxs-lookup"><span data-stu-id="fdfde-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="fdfde-108">[.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]</span><span class="sxs-lookup"><span data-stu-id="fdfde-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="fdfde-109">Свойство **\_ NewEnum** Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который можно использовать для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="fdfde-109">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="fdfde-110">Это свойство скрыто в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="fdfde-110">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="fdfde-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fdfde-111">Syntax</span></span>


```VB
ExtendedProperties._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="fdfde-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fdfde-112">Property value</span></span>

<span data-ttu-id="fdfde-113">Интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) объекта, который может использоваться для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="fdfde-113">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdfde-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fdfde-114">Remarks</span></span>

<span data-ttu-id="fdfde-115">Это свойство автоматически используется для внутренних целей при использовании `For Each In` конструкции в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="fdfde-115">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="fdfde-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fdfde-116">Requirements</span></span>



| <span data-ttu-id="fdfde-117">Требование</span><span class="sxs-lookup"><span data-stu-id="fdfde-117">Requirement</span></span> | <span data-ttu-id="fdfde-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fdfde-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdfde-119">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="fdfde-119">End of client support</span></span><br/> | <span data-ttu-id="fdfde-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fdfde-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fdfde-121">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="fdfde-121">End of server support</span></span><br/> | <span data-ttu-id="fdfde-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fdfde-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fdfde-123">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="fdfde-123">Redistributable</span></span><br/>       | <span data-ttu-id="fdfde-124">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="fdfde-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fdfde-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fdfde-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="fdfde-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdfde-126"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
