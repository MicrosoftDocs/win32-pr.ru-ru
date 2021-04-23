---
description: Представляет коллекцию объектов-подписывающих.
ms.assetid: 72e86acd-eb87-4eff-bd4e-327630ebbfc4
title: Объект подписывающих
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 75eba0ecb2592bf7efc27ecdd63288179e306651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665265"
---
# <a name="signers-object"></a><span data-ttu-id="b9251-103">Объект подписывающих</span><span class="sxs-lookup"><span data-stu-id="b9251-103">Signers object</span></span>

<span data-ttu-id="b9251-104">\[Объект- **подписавший** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="b9251-104">\[The **Signers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b9251-105">Вместо этого используйте коллекцию объектов Кмссигнер.</span><span class="sxs-lookup"><span data-stu-id="b9251-105">Instead, use a collection of CmsSigner objects.</span></span> <span data-ttu-id="b9251-106">Дополнительные сведения см. в описании [**класса кмссигнер**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="b9251-106">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="b9251-107">Объект- **подписавший** представляет коллекцию объектов- [**подписывающих**](signer.md) .</span><span class="sxs-lookup"><span data-stu-id="b9251-107">The **Signers** object represents a collection of [**Signer**](signer.md) objects.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="b9251-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="b9251-108">When to use</span></span>

<span data-ttu-id="b9251-109">Объект- **подписавший** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="b9251-109">The **Signers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="b9251-110">Получение числа сертификатов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="b9251-110">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="b9251-111">Получение конкретного объекта **подписывающих** из коллекции.</span><span class="sxs-lookup"><span data-stu-id="b9251-111">Retrieve a specific **Signers** object from the collection.</span></span>
-   <span data-ttu-id="b9251-112">Выполните итерацию по коллекции.</span><span class="sxs-lookup"><span data-stu-id="b9251-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="b9251-113">Элементы</span><span class="sxs-lookup"><span data-stu-id="b9251-113">Members</span></span>

<span data-ttu-id="b9251-114">Объект **подписывающих** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b9251-114">The **Signers** object has these types of members:</span></span>

-   [<span data-ttu-id="b9251-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="b9251-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b9251-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="b9251-116">Properties</span></span>

<span data-ttu-id="b9251-117">У объекта **подписывающих** есть эти свойства.</span><span class="sxs-lookup"><span data-stu-id="b9251-117">The **Signers** object has these properties.</span></span>



| <span data-ttu-id="b9251-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="b9251-118">Property</span></span>                                        | <span data-ttu-id="b9251-119">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="b9251-119">Access type</span></span>          | <span data-ttu-id="b9251-120">Описание</span><span class="sxs-lookup"><span data-stu-id="b9251-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9251-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="b9251-121">**\_NewEnum**</span></span>](signers-newenum.md)<br/> | <span data-ttu-id="b9251-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b9251-122">Read-only</span></span><br/> | <span data-ttu-id="b9251-123">Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который может быть использован для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="b9251-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="b9251-124">Это свойство скрыто в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="b9251-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="b9251-125">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="b9251-125">**Count**</span></span>](signers-count.md)<br/>       | <span data-ttu-id="b9251-126">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b9251-126">Read-only</span></span><br/> | <span data-ttu-id="b9251-127">Число объектов [**подписывающих**](signer.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="b9251-127">Number of [**Signer**](signer.md) objects in the collection.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="b9251-128">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b9251-128">**Item**</span></span>](signers-item.md)<br/>         | <span data-ttu-id="b9251-129">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b9251-129">Read-only</span></span><br/> | <span data-ttu-id="b9251-130">Извлекает объект [**подписавший**](signer.md) , представляющий индексированный подписывающий.</span><span class="sxs-lookup"><span data-stu-id="b9251-130">Retrieves the [**Signer**](signer.md) object that represents the indexed signer.</span></span> <span data-ttu-id="b9251-131">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b9251-131">This is the default property.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="b9251-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b9251-132">Remarks</span></span>

<span data-ttu-id="b9251-133">Не удается создать объект **подписывающих** .</span><span class="sxs-lookup"><span data-stu-id="b9251-133">The **Signers** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9251-134">Требования</span><span class="sxs-lookup"><span data-stu-id="b9251-134">Requirements</span></span>



| <span data-ttu-id="b9251-135">Требование</span><span class="sxs-lookup"><span data-stu-id="b9251-135">Requirement</span></span> | <span data-ttu-id="b9251-136">Значение</span><span class="sxs-lookup"><span data-stu-id="b9251-136">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9251-137">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="b9251-137">Redistributable</span></span><br/> | <span data-ttu-id="b9251-138">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="b9251-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b9251-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b9251-139">DLL</span></span><br/>             | <dl> <span data-ttu-id="b9251-140"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9251-140"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9251-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9251-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9251-142">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="b9251-142">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
