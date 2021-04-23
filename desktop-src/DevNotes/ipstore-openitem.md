---
description: Открывает элемент для нескольких обращений.
ms.assetid: b0602abd-dbda-40d0-befa-348c1179fa4f
title: 'Метод Ипсторе:: Опенитем (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.OpenItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 065b98c1f302596ce5a4a428ef2486e7cdcc2320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665097"
---
# <a name="ipstoreopenitem-method"></a><span data-ttu-id="edadd-103">Метод Ипсторе:: Опенитем</span><span class="sxs-lookup"><span data-stu-id="edadd-103">IPStore::OpenItem method</span></span>

<span data-ttu-id="edadd-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="edadd-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="edadd-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="edadd-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="edadd-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="edadd-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="edadd-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="edadd-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="edadd-108">Открывает элемент для нескольких обращений.</span><span class="sxs-lookup"><span data-stu-id="edadd-108">Opens an item for multiple accesses.</span></span>

## <a name="syntax"></a><span data-ttu-id="edadd-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="edadd-109">Syntax</span></span>


```C++
HRESULT OpenItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       PST_ACCESSMODE ModeFlags,
  [in]       PPST_PROMPTIFO pProomptInfo,
  [in]       DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="edadd-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="edadd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edadd-111">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="edadd-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edadd-112">Указывает, является ли тип локальным для компьютера или связан только с созданием пользователя.</span><span class="sxs-lookup"><span data-stu-id="edadd-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="edadd-113">Значение</span><span class="sxs-lookup"><span data-stu-id="edadd-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="edadd-114">Значение</span><span class="sxs-lookup"><span data-stu-id="edadd-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="edadd-115">PST-файл <dt>**\_ КЛЮЧ \_ текущего \_ пользователя**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="edadd-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="edadd-116">Хранилище сохраняется в разделе реестра текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="edadd-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="edadd-117">PST-файл <dt>**\_ КЛЮЧ \_ Локальная \_ машина**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="edadd-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="edadd-118">Хранилище сохраняется в разделе реестра локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="edadd-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="edadd-119">*питемтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="edadd-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edadd-120">Указатель на идентификатор GUID, определяющий тип данных открываемого элемента.</span><span class="sxs-lookup"><span data-stu-id="edadd-120">A pointer to a GUID that identifies the data type of the item to open.</span></span>

</dd> <dt>

<span data-ttu-id="edadd-121">*питемсубтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="edadd-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edadd-122">Указатель на идентификатор GUID, указывающий подтип элемента для открытия.</span><span class="sxs-lookup"><span data-stu-id="edadd-122">A pointer to a GUID that indicates the item subtype to open.</span></span>

</dd> <dt>

<span data-ttu-id="edadd-123">*сзитемнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="edadd-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edadd-124">Строка, содержащая имя открываемого элемента.</span><span class="sxs-lookup"><span data-stu-id="edadd-124">A string that contains the name of the item to open.</span></span>

</dd> <dt>

<span data-ttu-id="edadd-125">*Модефлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="edadd-125">*ModeFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edadd-126">Описывает режимы доступа, к которым относятся указанные наборы предложений доступа.</span><span class="sxs-lookup"><span data-stu-id="edadd-126">Describes the access modes to which a specified set of access clauses pertains.</span></span> <span data-ttu-id="edadd-127">Дополнительные сведения см. в разделе [**типы PStore**](pstore-types.md).</span><span class="sxs-lookup"><span data-stu-id="edadd-127">For more information, see [**PStore Types**](pstore-types.md).</span></span>



| <span data-ttu-id="edadd-128">Значение</span><span class="sxs-lookup"><span data-stu-id="edadd-128">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="edadd-129">Значение</span><span class="sxs-lookup"><span data-stu-id="edadd-129">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <span data-ttu-id="edadd-130">PST-файл <dt>**\_ ЧТЕНИЕ**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="edadd-130"><dt>**PST\_READ**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="edadd-131">Режим доступа для чтения.</span><span class="sxs-lookup"><span data-stu-id="edadd-131">Read access mode.</span></span><br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <span data-ttu-id="edadd-132">PST-файл <dt>**\_ ЗАПИСЬ**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="edadd-132"><dt>**PST\_WRITE**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="edadd-133">Режим доступа для записи.</span><span class="sxs-lookup"><span data-stu-id="edadd-133">Write access mode.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="edadd-134">*ппрумптинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="edadd-134">*pProomptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edadd-135">Указатель на структуру [**PST \_ промптинфо**](pst-promptinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="edadd-135">A pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="edadd-136">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="edadd-136">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edadd-137">Reserved: значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="edadd-137">Reserved: must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edadd-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="edadd-138">Return value</span></span>

<span data-ttu-id="edadd-139">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="edadd-139">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="edadd-140">Значение **PST \_ E \_ OK** указывает, что функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="edadd-140">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="edadd-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="edadd-141">Remarks</span></span>

<span data-ttu-id="edadd-142">Чтобы открыть элемент в защищенной базе данных хранилища с помощью **опенитем** , необходимо закрыть его с помощью [**Ипсторе:: клосеитем**](ipstore-closeitem.md) , чтобы предотвратить утечку памяти.</span><span class="sxs-lookup"><span data-stu-id="edadd-142">Using **OpenItem** to open an item in the protected storage database requires that it eventually be closed using [**IPStore::CloseItem**](ipstore-closeitem.md) to prevent a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="edadd-143">Требования</span><span class="sxs-lookup"><span data-stu-id="edadd-143">Requirements</span></span>



| <span data-ttu-id="edadd-144">Требование</span><span class="sxs-lookup"><span data-stu-id="edadd-144">Requirement</span></span> | <span data-ttu-id="edadd-145">Значение</span><span class="sxs-lookup"><span data-stu-id="edadd-145">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="edadd-146">Header</span><span class="sxs-lookup"><span data-stu-id="edadd-146">Header</span></span><br/> | <dl> <span data-ttu-id="edadd-147"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="edadd-147"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="edadd-148">DLL</span><span class="sxs-lookup"><span data-stu-id="edadd-148">DLL</span></span><br/>    | <dl> <span data-ttu-id="edadd-149"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edadd-149"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edadd-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="edadd-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edadd-151">**ипсторе**</span><span class="sxs-lookup"><span data-stu-id="edadd-151">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="edadd-152">**PST-файл \_ промптинфо**</span><span class="sxs-lookup"><span data-stu-id="edadd-152">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
