---
description: Добавляет объект сертификата в коллекцию получателей.
ms.assetid: 2a1b9e0f-ccbf-4042-871b-397de6b6fc35
title: Метод Recipients. Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 255d17485e3423d50cd86b092c2120605f0f1106
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665394"
---
# <a name="recipientsadd-method"></a><span data-ttu-id="ce241-103">Метод Recipients. Add</span><span class="sxs-lookup"><span data-stu-id="ce241-103">Recipients.Add method</span></span>

<span data-ttu-id="ce241-104">\[Метод **Add** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="ce241-104">\[The **Add** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ce241-105">Вместо этого используйте [**класс кмсреЦипиентколлектион**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="ce241-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="ce241-106">Метод **Add** добавляет объект [**сертификата**](certificate.md) в коллекцию [**получателей**](recipients.md) .</span><span class="sxs-lookup"><span data-stu-id="ce241-106">The **Add** method adds a [**Certificate**](certificate.md) object to a [**Recipients**](recipients.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce241-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce241-107">Syntax</span></span>


```VB
Recipients.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="ce241-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce241-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce241-109">*Сертификат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ce241-109">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce241-110">Выражение, которое разрешается в объект [**сертификата**](certificate.md) для добавления в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="ce241-110">Expression that resolves to the [**Certificate**](certificate.md) object to be added to the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce241-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce241-111">Return value</span></span>

<span data-ttu-id="ce241-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ce241-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce241-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ce241-113">Requirements</span></span>



| <span data-ttu-id="ce241-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ce241-114">Requirement</span></span> | <span data-ttu-id="ce241-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ce241-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce241-116">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="ce241-116">Redistributable</span></span><br/> | <span data-ttu-id="ce241-117">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="ce241-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ce241-118">DLL</span><span class="sxs-lookup"><span data-stu-id="ce241-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="ce241-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce241-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce241-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce241-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce241-121">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="ce241-121">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="ce241-122">**Recipients**</span><span class="sxs-lookup"><span data-stu-id="ce241-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
