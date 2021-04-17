---
description: '\_Свойство NewEnum атрибутов Извлекает интерфейс IEnumVARIANT для объекта, который можно использовать для перечисления коллекции. Это свойство скрыто в Visual Basic Scripting Edition (VBScript).'
ms.assetid: a90ef28b-3926-4542-bcd2-27f0eda4e339
title: Attributes._NewEnum, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9948c55943a8374665fe5e4883013742188665c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668696"
---
# <a name="attributes_newenum-property"></a><span data-ttu-id="fe975-104">Атрибуты. \_ Свойство NewEnum</span><span class="sxs-lookup"><span data-stu-id="fe975-104">Attributes.\_NewEnum property</span></span>

<span data-ttu-id="fe975-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fe975-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="fe975-106">Вместо этого используйте [**класс криптографикаттрибутеобжектколлектион**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="fe975-106">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="fe975-107">Свойство **\_ NewEnum** Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который можно использовать для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="fe975-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="fe975-108">Это свойство скрыто в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="fe975-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="fe975-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe975-109">Syntax</span></span>


```VB
Attributes._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="fe975-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fe975-110">Property value</span></span>

<span data-ttu-id="fe975-111">Интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) объекта, который может использоваться для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="fe975-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe975-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe975-112">Remarks</span></span>

<span data-ttu-id="fe975-113">Это свойство автоматически используется для внутренних целей при использовании `For Each In` конструкции в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="fe975-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe975-114">Требования</span><span class="sxs-lookup"><span data-stu-id="fe975-114">Requirements</span></span>



| <span data-ttu-id="fe975-115">Требование</span><span class="sxs-lookup"><span data-stu-id="fe975-115">Requirement</span></span> | <span data-ttu-id="fe975-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fe975-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe975-117">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="fe975-117">End of client support</span></span><br/> | <span data-ttu-id="fe975-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe975-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fe975-119">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="fe975-119">End of server support</span></span><br/> | <span data-ttu-id="fe975-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe975-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fe975-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="fe975-121">Redistributable</span></span><br/>       | <span data-ttu-id="fe975-122">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="fe975-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fe975-123">DLL</span><span class="sxs-lookup"><span data-stu-id="fe975-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="fe975-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe975-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe975-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe975-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe975-126">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="fe975-126">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
