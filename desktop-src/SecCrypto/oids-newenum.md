---
description: '\_Свойство NewEnum объектов Oid Извлекает интерфейс IEnumVARIANT для объекта, который можно использовать для перечисления коллекции. Это свойство скрыто в Visual Basic Scripting Edition (VBScript).'
ms.assetid: 7c09fd11-064b-451e-bd6b-e6c13ab228a0
title: OIDs._NewEnum, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d20856c17dda18a10b85c01453cbe043144742d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685181"
---
# <a name="oids_newenum-property"></a><span data-ttu-id="63bd5-104">OID. \_ Свойство NewEnum</span><span class="sxs-lookup"><span data-stu-id="63bd5-104">OIDs.\_NewEnum property</span></span>

<span data-ttu-id="63bd5-105">\[Свойство **\_ NewEnum** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="63bd5-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="63bd5-106">Вместо этого используйте [**класс оидколлектион**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="63bd5-106">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="63bd5-107">Свойство **\_ NewEnum** Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который можно использовать для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="63bd5-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="63bd5-108">Это свойство скрыто в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="63bd5-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="63bd5-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63bd5-109">Syntax</span></span>


```VB
OIDs._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="63bd5-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="63bd5-110">Property value</span></span>

<span data-ttu-id="63bd5-111">Интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) объекта, который может использоваться для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="63bd5-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="63bd5-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63bd5-112">Remarks</span></span>

<span data-ttu-id="63bd5-113">Это свойство автоматически используется для внутренних целей при использовании `For Each In` конструкции в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="63bd5-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="63bd5-114">Требования</span><span class="sxs-lookup"><span data-stu-id="63bd5-114">Requirements</span></span>



| <span data-ttu-id="63bd5-115">Требование</span><span class="sxs-lookup"><span data-stu-id="63bd5-115">Requirement</span></span> | <span data-ttu-id="63bd5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="63bd5-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63bd5-117">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="63bd5-117">Redistributable</span></span><br/> | <span data-ttu-id="63bd5-118">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="63bd5-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="63bd5-119">DLL</span><span class="sxs-lookup"><span data-stu-id="63bd5-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="63bd5-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63bd5-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63bd5-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63bd5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63bd5-122">**OID**</span><span class="sxs-lookup"><span data-stu-id="63bd5-122">**OIDs**</span></span>](oids.md)
</dt> </dl>

 

 
