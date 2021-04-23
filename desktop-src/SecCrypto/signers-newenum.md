---
description: '\_Свойство NewEnum подписавший Извлекает интерфейс IEnumVARIANT для объекта, который можно использовать для перечисления коллекции. Это свойство скрыто в Visual Basic Scripting Edition (VBScript).'
ms.assetid: 99d7ddd3-a552-4125-b220-d1b28f20d1ed
title: Signers._NewEnum, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 91007e7ce282cb44267927f54ab26f8f930028f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669109"
---
# <a name="signers_newenum-property"></a><span data-ttu-id="76030-104">Подписывающих. \_ Свойство NewEnum</span><span class="sxs-lookup"><span data-stu-id="76030-104">Signers.\_NewEnum property</span></span>

<span data-ttu-id="76030-105">\[Свойство **\_ NewEnum** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="76030-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="76030-106">Вместо этого используйте коллекцию объектов Кмссигнер.</span><span class="sxs-lookup"><span data-stu-id="76030-106">Instead, use a collection of CmsSigner objects.</span></span> <span data-ttu-id="76030-107">Дополнительные сведения см. в описании [**класса кмссигнер**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="76030-107">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="76030-108">Свойство **\_ NewEnum** Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который можно использовать для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="76030-108">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="76030-109">Это свойство скрыто в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="76030-109">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="76030-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76030-110">Syntax</span></span>


```VB
Signers._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="76030-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="76030-111">Property value</span></span>

<span data-ttu-id="76030-112">Интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) объекта, который может использоваться для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="76030-112">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="76030-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76030-113">Remarks</span></span>

<span data-ttu-id="76030-114">Это свойство автоматически используется для внутренних целей при использовании `For Each In` конструкции в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="76030-114">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="76030-115">Требования</span><span class="sxs-lookup"><span data-stu-id="76030-115">Requirements</span></span>



| <span data-ttu-id="76030-116">Требование</span><span class="sxs-lookup"><span data-stu-id="76030-116">Requirement</span></span> | <span data-ttu-id="76030-117">Значение</span><span class="sxs-lookup"><span data-stu-id="76030-117">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76030-118">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="76030-118">Redistributable</span></span><br/> | <span data-ttu-id="76030-119">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="76030-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="76030-120">DLL</span><span class="sxs-lookup"><span data-stu-id="76030-120">DLL</span></span><br/>             | <dl> <span data-ttu-id="76030-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76030-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76030-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76030-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76030-123">**Подписавшими**</span><span class="sxs-lookup"><span data-stu-id="76030-123">**Signers**</span></span>](signers.md)
</dt> </dl>

 

 
