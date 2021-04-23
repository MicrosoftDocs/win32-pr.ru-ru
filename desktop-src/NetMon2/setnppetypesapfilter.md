---
description: Задает фильтр для BLOB-объектов ETYPE/SAP.
ms.assetid: cd659c93-3415-4737-b848-936e80318544
title: Функция Сетнппетипесапфилтер (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 14657536e09b65912afa1715c296663d8d1916b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344962"
---
# <a name="setnppetypesapfilter-function"></a><span data-ttu-id="9c54a-103">Функция Сетнппетипесапфилтер</span><span class="sxs-lookup"><span data-stu-id="9c54a-103">SetNPPEtypeSapFilter function</span></span>

<span data-ttu-id="9c54a-104">Функция **сетнппетипесапфилтер** задает фильтр типа BLOB-объекта ETYPE/SAP.</span><span class="sxs-lookup"><span data-stu-id="9c54a-104">The **SetNPPEtypeSapFilter** function sets the BLOB Etype/Sap filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c54a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c54a-105">Syntax</span></span>


```C++
DWORD SetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _In_  WORD   nSaps,
  _In_  WORD   nEtypes,
  _In_  LPBYTE lpSapTable,
  _In_  LPWORD lpEtypeTable,
  _In_  DWORD  FilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="9c54a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c54a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c54a-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c54a-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c54a-108">Маркер для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="9c54a-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="9c54a-109">*нсапс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c54a-109">*nSaps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c54a-110">Число SAPs.</span><span class="sxs-lookup"><span data-stu-id="9c54a-110">The number of SAPs.</span></span>

</dd> <dt>

<span data-ttu-id="9c54a-111">*нетипес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c54a-111">*nEtypes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c54a-112">Число ETYPE в устанавливаемой таблице etype.</span><span class="sxs-lookup"><span data-stu-id="9c54a-112">The number of Etypes in the Etype table being set.</span></span>

</dd> <dt>

<span data-ttu-id="9c54a-113">*лпсаптабле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c54a-113">*lpSapTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c54a-114">Указатель на заданную таблицу SAP.</span><span class="sxs-lookup"><span data-stu-id="9c54a-114">A pointer to the SAP table that is set.</span></span>

</dd> <dt>

<span data-ttu-id="9c54a-115">*лпетипетабле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c54a-115">*lpEtypeTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c54a-116">Указатель на заданную таблицу etype.</span><span class="sxs-lookup"><span data-stu-id="9c54a-116">A pointer to the Etype table that is set.</span></span>

</dd> <dt>

<span data-ttu-id="9c54a-117">*Филтерфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c54a-117">*FilterFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c54a-118">Заданные флаги фильтра.</span><span class="sxs-lookup"><span data-stu-id="9c54a-118">The filter flags that are set.</span></span>

</dd> <dt>

<span data-ttu-id="9c54a-119">*херрорблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9c54a-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c54a-120">Маркер для большого двоичного объекта ошибки, указывающий, где в исходном большом двоичном объекте произошла ошибка (если таковая имеется).</span><span class="sxs-lookup"><span data-stu-id="9c54a-120">The handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c54a-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c54a-121">Return value</span></span>

<span data-ttu-id="9c54a-122">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="9c54a-122">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="9c54a-123">Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="9c54a-123">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c54a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="9c54a-124">Requirements</span></span>



| <span data-ttu-id="9c54a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="9c54a-125">Requirement</span></span> | <span data-ttu-id="9c54a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9c54a-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c54a-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c54a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9c54a-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9c54a-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9c54a-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c54a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9c54a-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9c54a-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9c54a-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9c54a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c54a-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c54a-132"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="9c54a-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9c54a-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="9c54a-134"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c54a-134"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="9c54a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9c54a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c54a-136"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c54a-136"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c54a-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c54a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c54a-138">жетнппетипесапфилтер</span><span class="sxs-lookup"><span data-stu-id="9c54a-138">GetNPPEtypeSapFilter</span></span>](getnppetypesapfilter.md)
</dt> </dl>

 

 




