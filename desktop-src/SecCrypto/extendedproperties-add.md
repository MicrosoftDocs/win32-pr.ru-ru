---
description: Добавляет расширенное свойство в коллекцию.
ms.assetid: 1d6b3c39-17b0-4a7c-a5c2-4a3bd866be07
title: Расширенных свойств. Add, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06e4170b34dcdca97bc0bae6bb48b4a057a8e9b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648867"
---
# <a name="extendedpropertiesadd-method"></a><span data-ttu-id="d0ea5-103">Расширенных свойств. Add, метод</span><span class="sxs-lookup"><span data-stu-id="d0ea5-103">ExtendedProperties.Add method</span></span>

<span data-ttu-id="d0ea5-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d0ea5-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d0ea5-105">Вместо этого используйте службы вызова платформы (PInvoke) для вызова функции Win32 API [**цертжетцертификатеконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) и получения свойств.</span><span class="sxs-lookup"><span data-stu-id="d0ea5-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="d0ea5-106">Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода.</span><span class="sxs-lookup"><span data-stu-id="d0ea5-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="d0ea5-107">[.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]</span><span class="sxs-lookup"><span data-stu-id="d0ea5-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="d0ea5-108">Метод **Add** добавляет расширенное свойство в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="d0ea5-108">The **Add** method adds an extended property to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0ea5-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0ea5-109">Syntax</span></span>


```VB
ExtendedProperties.Add( _
  ByVal valProperty _
)
```



## <a name="parameters"></a><span data-ttu-id="d0ea5-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0ea5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0ea5-111">*валпроперти* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d0ea5-111">*valProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0ea5-112">Объект [**ExtendedProperty**](extendedproperty.md) , представляющий расширенное свойство.</span><span class="sxs-lookup"><span data-stu-id="d0ea5-112">An [**ExtendedProperty**](extendedproperty.md) object that represents the extended property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0ea5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0ea5-113">Return value</span></span>

<span data-ttu-id="d0ea5-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d0ea5-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0ea5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d0ea5-115">Requirements</span></span>



| <span data-ttu-id="d0ea5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d0ea5-116">Requirement</span></span> | <span data-ttu-id="d0ea5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d0ea5-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0ea5-118">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d0ea5-118">End of client support</span></span><br/> | <span data-ttu-id="d0ea5-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0ea5-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d0ea5-120">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="d0ea5-120">End of server support</span></span><br/> | <span data-ttu-id="d0ea5-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0ea5-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d0ea5-122">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="d0ea5-122">Redistributable</span></span><br/>       | <span data-ttu-id="d0ea5-123">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="d0ea5-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d0ea5-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d0ea5-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d0ea5-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0ea5-125"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
