---
description: Функция Жетнппетипесапфилтер извлекает фильтр ETYPE или SAP из заданного большого двоичного объекта.
ms.assetid: c4891eff-ab2d-43ff-8d2b-3aa299570c0a
title: Функция Жетнппетипесапфилтер (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5359332d96fb85343300c5def12070c812bd99d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674488"
---
# <a name="getnppetypesapfilter-function"></a><span data-ttu-id="e3806-103">Функция Жетнппетипесапфилтер</span><span class="sxs-lookup"><span data-stu-id="e3806-103">GetNPPEtypeSapFilter function</span></span>

<span data-ttu-id="e3806-104">Функция **жетнппетипесапфилтер** извлекает фильтр ETYPE или SAP из заданного большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="e3806-104">The **GetNPPEtypeSapFilter** function retrieves the Etype/Sap filter from a given BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3806-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3806-105">Syntax</span></span>


```C++
DWORD GetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _Out_ WORD   *pnSaps,
  _Out_ WORD   *pnEtypes,
  _Out_ LPBYTE *ppSapTable,
  _Out_ LPWORD *ppEtypeTable,
  _Out_ DWORD  *pFilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="e3806-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3806-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3806-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e3806-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3806-108">Обработчик для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="e3806-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="e3806-109">*пнсапс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e3806-109">*pnSaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3806-110">Указатель на возвращенное число протоколов в таблице SAP.</span><span class="sxs-lookup"><span data-stu-id="e3806-110">Pointer to the returned number of protocols in the SAP table.</span></span>

</dd> <dt>

<span data-ttu-id="e3806-111">*пнетипес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e3806-111">*pnEtypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3806-112">Указатель на возвращенное число ETYPE в таблице etype.</span><span class="sxs-lookup"><span data-stu-id="e3806-112">Pointer to the returned number of Etypes in the Etype table.</span></span>

</dd> <dt>

<span data-ttu-id="e3806-113">*ппсаптабле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e3806-113">*ppSapTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3806-114">Указатель на возвращенную таблицу SAP.</span><span class="sxs-lookup"><span data-stu-id="e3806-114">Pointer to the returned SAP table.</span></span>

</dd> <dt>

<span data-ttu-id="e3806-115">*ппетипетабле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e3806-115">*ppEtypeTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3806-116">Указатель на возвращенную таблицу etype.</span><span class="sxs-lookup"><span data-stu-id="e3806-116">Pointer to the returned Etype table.</span></span>

</dd> <dt>

<span data-ttu-id="e3806-117">*пфилтерфлагс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e3806-117">*pFilterFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3806-118">Указатель на возвращаемые флаги фильтра.</span><span class="sxs-lookup"><span data-stu-id="e3806-118">Pointer to the returned filter flags.</span></span>

</dd> <dt>

<span data-ttu-id="e3806-119">*херрорблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e3806-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3806-120">Обработайте с BLOB-объектом ошибок, который указывает расположение в исходном большом двоичном объекте, где произошла ошибка (если таковая имеется).</span><span class="sxs-lookup"><span data-stu-id="e3806-120">Handle to an error BLOB, which specifies the location in the original BLOB where the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3806-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3806-121">Return value</span></span>

<span data-ttu-id="e3806-122">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e3806-122">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e3806-123">Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="e3806-123">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3806-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3806-124">Remarks</span></span>

<span data-ttu-id="e3806-125">Информация ETYPE/SAP хранится в категории **config** раздела НПП **owner** .</span><span class="sxs-lookup"><span data-stu-id="e3806-125">The Etype/Sap information is stored in the **Config** category of the NPP **Owner** section.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3806-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e3806-126">Requirements</span></span>



| <span data-ttu-id="e3806-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e3806-127">Requirement</span></span> | <span data-ttu-id="e3806-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e3806-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3806-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3806-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e3806-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e3806-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e3806-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3806-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e3806-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e3806-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e3806-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e3806-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3806-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3806-134"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="e3806-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e3806-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="e3806-136"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3806-136"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="e3806-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e3806-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3806-138"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3806-138"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3806-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3806-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3806-140">сетнппетипесапфилтер</span><span class="sxs-lookup"><span data-stu-id="e3806-140">SetNPPEtypeSapFilter</span></span>](setnppetypesapfilter.md)
</dt> </dl>

 

 




