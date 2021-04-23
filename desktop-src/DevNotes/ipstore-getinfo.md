---
description: Возвращает сведения о поставщике хранилища.
ms.assetid: bdacb5bb-a37a-4970-add7-57625bec1ce0
title: Метод Ипсторе::-info (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7747c3acf15a60f5556a8855ef4825715ef5050b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665098"
---
# <a name="ipstoregetinfo-method"></a><span data-ttu-id="587d1-103">Метод Ипсторе:: info</span><span class="sxs-lookup"><span data-stu-id="587d1-103">IPStore::GetInfo method</span></span>

<span data-ttu-id="587d1-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="587d1-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="587d1-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="587d1-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="587d1-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="587d1-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="587d1-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="587d1-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="587d1-108">Возвращает сведения о поставщике хранилища.</span><span class="sxs-lookup"><span data-stu-id="587d1-108">Returns information on the storage provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="587d1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="587d1-109">Syntax</span></span>


```C++
HRESULT GetInfo(
  [out] PPST_PROVIDERINFO *ppProperties
);
```



## <a name="parameters"></a><span data-ttu-id="587d1-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="587d1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="587d1-111">*пппропертиес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="587d1-111">*ppProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="587d1-112">Указатель на структуру **\_ провидеринфо ппст** , содержащую сведения о поставщике хранилища.</span><span class="sxs-lookup"><span data-stu-id="587d1-112">A pointer to a **PPST\_PROVIDERINFO** structure that contains information about the storage provider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="587d1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="587d1-113">Return value</span></span>

<span data-ttu-id="587d1-114">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="587d1-114">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="587d1-115">Значение **PST \_ E \_ OK** указывает, что функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="587d1-115">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="587d1-116">Требования</span><span class="sxs-lookup"><span data-stu-id="587d1-116">Requirements</span></span>



| <span data-ttu-id="587d1-117">Требование</span><span class="sxs-lookup"><span data-stu-id="587d1-117">Requirement</span></span> | <span data-ttu-id="587d1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="587d1-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="587d1-119">Header</span><span class="sxs-lookup"><span data-stu-id="587d1-119">Header</span></span><br/> | <dl> <span data-ttu-id="587d1-120"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="587d1-120"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="587d1-121">DLL</span><span class="sxs-lookup"><span data-stu-id="587d1-121">DLL</span></span><br/>    | <dl> <span data-ttu-id="587d1-122"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="587d1-122"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="587d1-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="587d1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="587d1-124">**ипсторе**</span><span class="sxs-lookup"><span data-stu-id="587d1-124">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
