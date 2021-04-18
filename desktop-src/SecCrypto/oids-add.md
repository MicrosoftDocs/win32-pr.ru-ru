---
description: Добавляет указанный объект OID в коллекцию.
ms.assetid: 0ae087d6-768a-4538-b834-0f936680de05
title: Метод OID. Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d2fa007798a0657991ec8e37a7dddc9fb4c95b2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688983"
---
# <a name="oidsadd-method"></a><span data-ttu-id="bff09-103">Метод OID. Add</span><span class="sxs-lookup"><span data-stu-id="bff09-103">OIDs.Add method</span></span>

<span data-ttu-id="bff09-104">\[Метод **Add** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="bff09-104">\[The **Add** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bff09-105">Вместо этого используйте [**класс оидколлектион**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="bff09-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="bff09-106">Метод **Add** добавляет указанный объект [**OID**](oid.md) в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="bff09-106">The **Add** method adds the specified [**OID**](oid.md) object to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bff09-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bff09-107">Syntax</span></span>


```VB
OIDs.Add( _
  ByVal OID _
)
```



## <a name="parameters"></a><span data-ttu-id="bff09-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bff09-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bff09-109">*Идентификатор объекта* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bff09-109">*OID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bff09-110">Объект [**OID**](oid.md) , добавляемый в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="bff09-110">The [**OID**](oid.md) object to be added to the collection.</span></span> <span data-ttu-id="bff09-111">Объект **OID** добавляется в отсортированном порядке на основе его точечного значения.</span><span class="sxs-lookup"><span data-stu-id="bff09-111">The **OID** object is added in sorted order based on its dotted value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bff09-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bff09-112">Return value</span></span>

<span data-ttu-id="bff09-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bff09-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bff09-114">Требования</span><span class="sxs-lookup"><span data-stu-id="bff09-114">Requirements</span></span>



| <span data-ttu-id="bff09-115">Требование</span><span class="sxs-lookup"><span data-stu-id="bff09-115">Requirement</span></span> | <span data-ttu-id="bff09-116">Значение</span><span class="sxs-lookup"><span data-stu-id="bff09-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bff09-117">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="bff09-117">Redistributable</span></span><br/> | <span data-ttu-id="bff09-118">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="bff09-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bff09-119">DLL</span><span class="sxs-lookup"><span data-stu-id="bff09-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="bff09-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bff09-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
