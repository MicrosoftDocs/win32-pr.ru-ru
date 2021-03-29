---
description: '\_Свойство NewEnum для EKU Извлекает интерфейс IEnumVARIANT для объекта, который можно использовать для перечисления коллекции. Это свойство скрыто в Visual Basic Scripting Edition (VBScript).'
ms.assetid: c7d038c0-416f-47f7-94ba-74ca877da7ba
title: EKUs._NewEnum, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 72605e0ad7bbb8671ff9a5885a79f1d7836c6efb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647909"
---
# <a name="ekus_newenum-property"></a><span data-ttu-id="a05e3-104">EKU. \_ Свойство NewEnum</span><span class="sxs-lookup"><span data-stu-id="a05e3-104">EKUs.\_NewEnum property</span></span>

<span data-ttu-id="a05e3-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a05e3-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a05e3-106">Вместо этого используйте [**класс X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a05e3-106">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a05e3-107">Свойство **\_ NewEnum** Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который можно использовать для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="a05e3-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="a05e3-108">Это свойство скрыто в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="a05e3-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="a05e3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a05e3-109">Syntax</span></span>


```VB
EKUs._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="a05e3-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a05e3-110">Property value</span></span>

<span data-ttu-id="a05e3-111">Интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) объекта, который может использоваться для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="a05e3-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="a05e3-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a05e3-112">Remarks</span></span>

<span data-ttu-id="a05e3-113">Это свойство автоматически используется для внутренних целей при использовании `For Each In` конструкции в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="a05e3-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="a05e3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a05e3-114">Requirements</span></span>



| <span data-ttu-id="a05e3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a05e3-115">Requirement</span></span> | <span data-ttu-id="a05e3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a05e3-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a05e3-117">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a05e3-117">End of client support</span></span><br/> | <span data-ttu-id="a05e3-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a05e3-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a05e3-119">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a05e3-119">End of server support</span></span><br/> | <span data-ttu-id="a05e3-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a05e3-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a05e3-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a05e3-121">Redistributable</span></span><br/>       | <span data-ttu-id="a05e3-122">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="a05e3-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a05e3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a05e3-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a05e3-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a05e3-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a05e3-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a05e3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a05e3-126">**EKU**</span><span class="sxs-lookup"><span data-stu-id="a05e3-126">**EKUs**</span></span>](ekus.md)
</dt> </dl>

 

 
