---
description: Выполняет сброс до начала последовательности перечисления.
ms.assetid: 9c5044b5-25a3-4d10-829b-ef4d8b5ac095
title: 'Метод Иенумпсторепровидерс:: Reset (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 2a5171820eb0f1e1326873b99b6b0d03fe289c5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648085"
---
# <a name="ienumpstoreprovidersreset-method"></a><span data-ttu-id="0066e-103">Метод Иенумпсторепровидерс:: Reset</span><span class="sxs-lookup"><span data-stu-id="0066e-103">IEnumPStoreProviders::Reset method</span></span>

<span data-ttu-id="0066e-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0066e-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="0066e-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="0066e-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="0066e-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="0066e-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="0066e-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="0066e-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="0066e-108">Выполняет сброс до начала последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="0066e-108">Resets to the beginning of the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="0066e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0066e-109">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="0066e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="0066e-110">Parameters</span></span>

<span data-ttu-id="0066e-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0066e-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0066e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0066e-112">Return value</span></span>

<span data-ttu-id="0066e-113">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0066e-113">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0066e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0066e-114">Requirements</span></span>



| <span data-ttu-id="0066e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="0066e-115">Requirement</span></span> | <span data-ttu-id="0066e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0066e-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0066e-117">Header</span><span class="sxs-lookup"><span data-stu-id="0066e-117">Header</span></span><br/> | <dl> <span data-ttu-id="0066e-118"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="0066e-118"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="0066e-119">DLL</span><span class="sxs-lookup"><span data-stu-id="0066e-119">DLL</span></span><br/>    | <dl> <span data-ttu-id="0066e-120"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0066e-120"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0066e-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0066e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0066e-122">**иенумпсторепровидерс**</span><span class="sxs-lookup"><span data-stu-id="0066e-122">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
