---
description: Возвращает указатель интерфейса подтипа для перечисления элементов в защищенной базе данных хранилища.
ms.assetid: 940c321d-ec14-43fd-841b-cf581796bc87
title: 'Метод Ипсторе:: Енумитемс (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 9b44ee41a7daa4a75a19ca0f7045d69f5b380c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648096"
---
# <a name="ipstoreenumitems-method"></a><span data-ttu-id="27c7f-103">Метод Ипсторе:: Енумитемс</span><span class="sxs-lookup"><span data-stu-id="27c7f-103">IPStore::EnumItems method</span></span>

<span data-ttu-id="27c7f-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="27c7f-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="27c7f-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="27c7f-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="27c7f-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="27c7f-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="27c7f-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="27c7f-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="27c7f-108">Возвращает указатель интерфейса подтипа для перечисления элементов в защищенной базе данных хранилища.</span><span class="sxs-lookup"><span data-stu-id="27c7f-108">Returns the interface pointer of a subtype for enumerating items in the protected storage database.</span></span>

## <a name="syntax"></a><span data-ttu-id="27c7f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27c7f-109">Syntax</span></span>


```C++
HRESULT EnumItems(
  [in]       PST_KEY          Key,
  [in] const PSGUID           *pItemType,
  [in] const GUID             *pItemSubtype,
  [in]       DWORD            dwFlags,
  [in]       IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="27c7f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="27c7f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27c7f-111">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="27c7f-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27c7f-112">Указывает, является ли тип локальным для компьютера или связан только с созданием пользователя.</span><span class="sxs-lookup"><span data-stu-id="27c7f-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="27c7f-113">Значение</span><span class="sxs-lookup"><span data-stu-id="27c7f-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="27c7f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="27c7f-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="27c7f-115">PST-файл <dt>**\_ КЛЮЧ \_ текущего \_ пользователя**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="27c7f-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="27c7f-116">Хранилище сохраняется в разделе реестра текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="27c7f-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="27c7f-117">PST-файл <dt>**\_ КЛЮЧ \_ Локальная \_ машина**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="27c7f-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="27c7f-118">Хранилище сохраняется в разделе реестра локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="27c7f-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="27c7f-119">*питемтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="27c7f-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27c7f-120">Указатель на **идентификатор GUID** , определяющий тип данных элемента для перечисления.</span><span class="sxs-lookup"><span data-stu-id="27c7f-120">A pointer to a **GUID** that identifies the data type of the item to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="27c7f-121">*питемсубтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="27c7f-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27c7f-122">Указатель на **идентификатор GUID** , определяющий подтип данных элемента для перечисления.</span><span class="sxs-lookup"><span data-stu-id="27c7f-122">A pointer to a **GUID** that identifies the data subtype of the item to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="27c7f-123">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="27c7f-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27c7f-124">Reserved: значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="27c7f-124">Reserved: Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="27c7f-125">*ппенум* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="27c7f-125">*ppenum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27c7f-126">Указатель на указатель на интерфейс [**иенумпстореитемс**](ienumpstoreitems.md) .</span><span class="sxs-lookup"><span data-stu-id="27c7f-126">A pointer to a pointer to an [**IEnumPStoreItems**](ienumpstoreitems.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27c7f-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="27c7f-127">Return value</span></span>

<span data-ttu-id="27c7f-128">Возвращаемое значение является значением **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="27c7f-128">The return value is an **HRESULT**.</span></span> <span data-ttu-id="27c7f-129">Значение **PST \_ E \_ OK** указывает, что функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="27c7f-129">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="27c7f-130">Требования</span><span class="sxs-lookup"><span data-stu-id="27c7f-130">Requirements</span></span>



| <span data-ttu-id="27c7f-131">Требование</span><span class="sxs-lookup"><span data-stu-id="27c7f-131">Requirement</span></span> | <span data-ttu-id="27c7f-132">Значение</span><span class="sxs-lookup"><span data-stu-id="27c7f-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27c7f-133">Header</span><span class="sxs-lookup"><span data-stu-id="27c7f-133">Header</span></span><br/> | <dl> <span data-ttu-id="27c7f-134"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="27c7f-134"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="27c7f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="27c7f-135">DLL</span></span><br/>    | <dl> <span data-ttu-id="27c7f-136"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27c7f-136"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27c7f-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27c7f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27c7f-138">**ипсторе**</span><span class="sxs-lookup"><span data-stu-id="27c7f-138">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
