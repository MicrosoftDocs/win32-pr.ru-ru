---
description: '\_Свойство NewEnum квалификаторов Извлекает интерфейс IEnumVARIANT для объекта, который можно использовать для перечисления коллекции. Это свойство скрыто в Visual Basic Scripting Edition (VBScript).'
ms.assetid: e51f8ca1-ef1f-475b-8368-e8296fae0f04
title: Qualifiers._NewEnum, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 01a4d62604dabacd2d78d5d2f6cbee0db7189196
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685386"
---
# <a name="qualifiers_newenum-property"></a><span data-ttu-id="8d9ab-104">Квалификаторы. \_ Свойство NewEnum</span><span class="sxs-lookup"><span data-stu-id="8d9ab-104">Qualifiers.\_NewEnum property</span></span>

<span data-ttu-id="8d9ab-105">\[Свойство **\_ NewEnum** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="8d9ab-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8d9ab-106">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для обработки квалификаторов, которые являются частью сведений о политике в расширении политик сертификатов.\]</span><span class="sxs-lookup"><span data-stu-id="8d9ab-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="8d9ab-107">Свойство **\_ NewEnum** Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который можно использовать для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="8d9ab-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="8d9ab-108">Это свойство скрыто в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="8d9ab-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="8d9ab-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d9ab-109">Syntax</span></span>


```VB
Qualifiers._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="8d9ab-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8d9ab-110">Property value</span></span>

<span data-ttu-id="8d9ab-111">Интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) объекта, который может использоваться для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="8d9ab-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d9ab-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d9ab-112">Remarks</span></span>

<span data-ttu-id="8d9ab-113">Это свойство автоматически используется для внутренних целей при использовании `For Each In` конструкции в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="8d9ab-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d9ab-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8d9ab-114">Requirements</span></span>



| <span data-ttu-id="8d9ab-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8d9ab-115">Requirement</span></span> | <span data-ttu-id="8d9ab-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8d9ab-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d9ab-117">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="8d9ab-117">Redistributable</span></span><br/> | <span data-ttu-id="8d9ab-118">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="8d9ab-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8d9ab-119">DLL</span><span class="sxs-lookup"><span data-stu-id="8d9ab-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="8d9ab-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d9ab-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d9ab-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d9ab-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d9ab-122">**Квалификаторы**</span><span class="sxs-lookup"><span data-stu-id="8d9ab-122">**Qualifiers**</span></span>](qualifiers.md)
</dt> </dl>

 

 
