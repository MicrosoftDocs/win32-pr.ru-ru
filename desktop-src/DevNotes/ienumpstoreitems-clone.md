---
description: 'Метод Иенумпстореитемс:: Clone — создает еще один перечислитель, который содержит то же состояние перечисления, что и текущий.'
ms.assetid: ab9eaf63-54e4-4322-9bb5-227982b15c73
title: 'Метод Иенумпстореитемс:: Clone (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 29b618881305296a560dc9102f7571c08236d1bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089332"
---
# <a name="ienumpstoreitemsclone-method"></a><span data-ttu-id="a7b71-103">Метод Иенумпстореитемс:: Clone</span><span class="sxs-lookup"><span data-stu-id="a7b71-103">IEnumPStoreItems::Clone method</span></span>

<span data-ttu-id="a7b71-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a7b71-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="a7b71-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="a7b71-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="a7b71-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="a7b71-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="a7b71-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="a7b71-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="a7b71-108">Создает другой перечислитель с тем же состоянием перечисления, что и текущий.</span><span class="sxs-lookup"><span data-stu-id="a7b71-108">Creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7b71-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7b71-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="a7b71-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7b71-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7b71-111">*ппенум* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a7b71-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7b71-112">Указатель на указатель [**иенумпстореитемс**](ienumpstoreitems.md) .</span><span class="sxs-lookup"><span data-stu-id="a7b71-112">A pointer to an [**IEnumPStoreItems**](ienumpstoreitems.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7b71-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7b71-113">Return value</span></span>

<span data-ttu-id="a7b71-114">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a7b71-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7b71-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a7b71-115">Requirements</span></span>



| <span data-ttu-id="a7b71-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a7b71-116">Requirement</span></span> | <span data-ttu-id="a7b71-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a7b71-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7b71-118">Header</span><span class="sxs-lookup"><span data-stu-id="a7b71-118">Header</span></span><br/> | <dl> <span data-ttu-id="a7b71-119"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7b71-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="a7b71-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a7b71-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="a7b71-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7b71-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7b71-122">См. также</span><span class="sxs-lookup"><span data-stu-id="a7b71-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7b71-123">**иенумпстореитемс**</span><span class="sxs-lookup"><span data-stu-id="a7b71-123">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
