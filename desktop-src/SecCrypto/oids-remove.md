---
description: Удаляет указанный объект OID из коллекции.
ms.assetid: c5eb6831-b195-4dc1-a6bd-d4245f9b0213
title: Метод OID. Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 000310e0034d413dea16a45f79647c3e0f7cf52d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685179"
---
# <a name="oidsremove-method"></a><span data-ttu-id="cbdd5-103">Метод OID. Remove</span><span class="sxs-lookup"><span data-stu-id="cbdd5-103">OIDs.Remove method</span></span>

<span data-ttu-id="cbdd5-104">\[Метод **Remove** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-104">\[The **Remove** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cbdd5-105">Вместо этого используйте [**класс оидколлектион**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="cbdd5-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="cbdd5-106">Метод **Remove** удаляет указанный объект [**OID**](oid.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-106">The **Remove** method removes the specified [**OID**](oid.md) object from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbdd5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbdd5-107">Syntax</span></span>


```VB
OIDs.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="cbdd5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbdd5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbdd5-109">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cbdd5-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbdd5-110">Индекс объекта [**OID**](oid.md) , который необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-110">Index of the [**OID**](oid.md) object to be removed.</span></span> <span data-ttu-id="cbdd5-111">Это может быть либо индекс в коллекции, либо точечное значение OID.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-111">This can be either an index into the collection or the dotted value of the OID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbdd5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbdd5-112">Return value</span></span>

<span data-ttu-id="cbdd5-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbdd5-114">Требования</span><span class="sxs-lookup"><span data-stu-id="cbdd5-114">Requirements</span></span>



| <span data-ttu-id="cbdd5-115">Требование</span><span class="sxs-lookup"><span data-stu-id="cbdd5-115">Requirement</span></span> | <span data-ttu-id="cbdd5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="cbdd5-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbdd5-117">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="cbdd5-117">Redistributable</span></span><br/> | <span data-ttu-id="cbdd5-118">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="cbdd5-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cbdd5-119">DLL</span><span class="sxs-lookup"><span data-stu-id="cbdd5-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="cbdd5-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbdd5-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
