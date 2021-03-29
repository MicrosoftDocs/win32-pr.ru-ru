---
description: Представляет свойство, расширенное корпорацией Майкрософт.
ms.assetid: 91375fd5-b3af-4ed4-961d-5cc1db1a14e3
title: Объект ExtendedProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperty
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ec61da301dc1819c899a7da23da9a10efd81ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668711"
---
# <a name="extendedproperty-object"></a><span data-ttu-id="687f8-103">Объект ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="687f8-103">ExtendedProperty object</span></span>

<span data-ttu-id="687f8-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="687f8-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="687f8-105">Вместо этого используйте службы вызова платформы (PInvoke) для вызова функции Win32 API [**цертжетцертификатеконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) и получения свойств.</span><span class="sxs-lookup"><span data-stu-id="687f8-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="687f8-106">Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода.</span><span class="sxs-lookup"><span data-stu-id="687f8-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="687f8-107">[.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]</span><span class="sxs-lookup"><span data-stu-id="687f8-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="687f8-108">Объект **ExtendedProperty** представляет свойство, расширенное корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="687f8-108">The **ExtendedProperty** object represents a Microsoft-extended property.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="687f8-109">Назначение</span><span class="sxs-lookup"><span data-stu-id="687f8-109">When to use</span></span>

<span data-ttu-id="687f8-110">Объект **ExtendedProperty** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="687f8-110">The **ExtendedProperty** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="687f8-111">Задайте или получите тип расширенного свойства.</span><span class="sxs-lookup"><span data-stu-id="687f8-111">Set or retrieve the type of the extended property.</span></span>
-   <span data-ttu-id="687f8-112">Установка или получение типа кодировки, используемой для кодирования расширенного свойства.</span><span class="sxs-lookup"><span data-stu-id="687f8-112">Set or retrieve the type of encoding used to encode the extended property.</span></span>

## <a name="members"></a><span data-ttu-id="687f8-113">Элементы</span><span class="sxs-lookup"><span data-stu-id="687f8-113">Members</span></span>

<span data-ttu-id="687f8-114">Объект **ExtendedProperty** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="687f8-114">The **ExtendedProperty** object has these types of members:</span></span>

-   [<span data-ttu-id="687f8-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="687f8-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="687f8-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="687f8-116">Properties</span></span>

<span data-ttu-id="687f8-117">Объект **ExtendedProperty** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="687f8-117">The **ExtendedProperty** object has these properties.</span></span>



| <span data-ttu-id="687f8-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="687f8-118">Property</span></span>                                             | <span data-ttu-id="687f8-119">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="687f8-119">Access type</span></span>           | <span data-ttu-id="687f8-120">Описание</span><span class="sxs-lookup"><span data-stu-id="687f8-120">Description</span></span>                                                                                                                                                                    |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="687f8-121">**PropID**</span><span class="sxs-lookup"><span data-stu-id="687f8-121">**PropID**</span></span>](extendedproperty-propid.md)<br/> | <span data-ttu-id="687f8-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="687f8-122">Read/write</span></span><br/> | <span data-ttu-id="687f8-123">Значение перечисления [**CAPICOM \_ PropID**](capicom-propid.md) , которое задает или получает тип расширенного свойства.</span><span class="sxs-lookup"><span data-stu-id="687f8-123">A value of the [**CAPICOM\_PROPID**](capicom-propid.md) enumeration that sets or retrieves the type of extended property.</span></span><br/> <span data-ttu-id="687f8-124">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="687f8-124">This is the default property.</span></span><br/> |
| [<span data-ttu-id="687f8-125">**Значение**</span><span class="sxs-lookup"><span data-stu-id="687f8-125">**Value**</span></span>](extendedproperty-value.md)<br/>   | <span data-ttu-id="687f8-126">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="687f8-126">Read/write</span></span><br/> | <span data-ttu-id="687f8-127">Значение перечисления [**\_ \_ типа CAPICOM Encoding**](capicom-encoding-type.md) , которое задает или получает данные расширенного свойства.</span><span class="sxs-lookup"><span data-stu-id="687f8-127">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that sets or retrieves the extended property data.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="687f8-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="687f8-128">Remarks</span></span>

<span data-ttu-id="687f8-129">Объект **ExtendedProperty** используется коллекцией [**расширенных свойств**](extendedproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="687f8-129">The **ExtendedProperty** object is used by the [**ExtendedProperties**](extendedproperties.md) collection.</span></span>

<span data-ttu-id="687f8-130">Объект **ExtendedProperty** может быть создан и не является надежным для скриптов.</span><span class="sxs-lookup"><span data-stu-id="687f8-130">The **ExtendedProperty** object can be created, and it is not safe for scripting.</span></span> <span data-ttu-id="687f8-131">ProgID для объекта **ExtendedProperty** — CAPICOM. ExtendedProperty. 1.</span><span class="sxs-lookup"><span data-stu-id="687f8-131">The ProgID for the **ExtendedProperty** object is CAPICOM.ExtendedProperty.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="687f8-132">Требования</span><span class="sxs-lookup"><span data-stu-id="687f8-132">Requirements</span></span>



| <span data-ttu-id="687f8-133">Требование</span><span class="sxs-lookup"><span data-stu-id="687f8-133">Requirement</span></span> | <span data-ttu-id="687f8-134">Значение</span><span class="sxs-lookup"><span data-stu-id="687f8-134">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="687f8-135">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="687f8-135">End of client support</span></span><br/> | <span data-ttu-id="687f8-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="687f8-136">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="687f8-137">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="687f8-137">End of server support</span></span><br/> | <span data-ttu-id="687f8-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="687f8-138">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="687f8-139">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="687f8-139">Redistributable</span></span><br/>       | <span data-ttu-id="687f8-140">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="687f8-140">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="687f8-141">DLL</span><span class="sxs-lookup"><span data-stu-id="687f8-141">DLL</span></span><br/>                   | <dl> <span data-ttu-id="687f8-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="687f8-142"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
