---
description: Функция Селектнппблобфромтабле выбирает сетевую карту из указанной таблицы BLOB-объектов НПП.
ms.assetid: 7f8010ed-472a-49b2-8d97-92851b6c14cd
title: Функция Селектнппблобфромтабле (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectNPPBlobFromTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d8f504d76d43b8a398947f435f7bd488678ea394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263237"
---
# <a name="selectnppblobfromtable-function"></a><span data-ttu-id="41e01-103">Функция Селектнппблобфромтабле</span><span class="sxs-lookup"><span data-stu-id="41e01-103">SelectNPPBlobFromTable function</span></span>

<span data-ttu-id="41e01-104">Функция **селектнппблобфромтабле** выбирает сетевую карту из указанной таблицы BLOB-объектов НПП.</span><span class="sxs-lookup"><span data-stu-id="41e01-104">The **SelectNPPBlobFromTable** function selects a NIC from a supplied NPP BLOB table.</span></span>

## <a name="syntax"></a><span data-ttu-id="41e01-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41e01-105">Syntax</span></span>


```C++
DWORD SelectNPPBlobFromTable(
  _In_  HWND        hwnd,
  _In_  PBLOB_TABLE pBlobTable,
  _Out_ HBLOB       *hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="41e01-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="41e01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41e01-107">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41e01-107">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41e01-108">Обработчик для окна, отображающего диалоговое окно **Выбор сети** .</span><span class="sxs-lookup"><span data-stu-id="41e01-108">Handle to the window that displays the **Select a network** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="41e01-109">*пблобтабле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41e01-109">*pBlobTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41e01-110">Указатель на переданную таблицу BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="41e01-110">Pointer to the supplied BLOB table.</span></span> <span data-ttu-id="41e01-111">Сетевой монитор использует эту таблицу для заполнения диалогового окна « **Выбор сети** ».</span><span class="sxs-lookup"><span data-stu-id="41e01-111">Network Monitor uses this table to populate the **Select a network** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="41e01-112">*хблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="41e01-112">*hBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41e01-113">Обработчик для большого двоичного объекта, представляющего выбранную сетевую карту.</span><span class="sxs-lookup"><span data-stu-id="41e01-113">Handle to the BLOB that represents the selected NIC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41e01-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41e01-114">Return value</span></span>

<span data-ttu-id="41e01-115">Если функция выполнена успешно и пользователь выбирает сетевую карту, возвращаемое значение — НМЕРР \_ Success; BLOB-объект, на который указывает *хблоб* , заполнен.</span><span class="sxs-lookup"><span data-stu-id="41e01-115">If the function is successful and the user selects a NIC, the return value is NMERR\_SUCCESS; the BLOB pointed to by *hBlob* is filled in.</span></span>

<span data-ttu-id="41e01-116">Если пользователь не выбрал сетевую карту, возвращается значение НМЕРР \_ No \_ НПП \_ .</span><span class="sxs-lookup"><span data-stu-id="41e01-116">If the user does not select a NIC, the return value is NMERR\_NO\_NPP\_SELECTED.</span></span>

<span data-ttu-id="41e01-117">Если функция завершается неудачно, возвращается значение другого НМЕРР.</span><span class="sxs-lookup"><span data-stu-id="41e01-117">If the function is unsuccessful, the return value is another NMERR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41e01-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41e01-118">Remarks</span></span>

<span data-ttu-id="41e01-119">При вызове сетевой монитор отображает диалоговое окно **Выбор сети** , которое можно использовать для выбора сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="41e01-119">When called, Network Monitor displays the **Select a network** dialog box, which you can use to select a NIC.</span></span> <span data-ttu-id="41e01-120">Большой двоичный объект НПП, представляющий выбранный сетевой адаптер, возвращается вызывающему приложению.</span><span class="sxs-lookup"><span data-stu-id="41e01-120">The NPP BLOB that represents the selected NIC returns to the calling application.</span></span>

<span data-ttu-id="41e01-121">Чтобы узнать о различных способах выбора сетевых интерфейсов, см. раздел [Выбор сетевой карты](selecting-a-network-interface-card.md) .</span><span class="sxs-lookup"><span data-stu-id="41e01-121">To learn the various ways you can select NICs, see [Selecting a Network Interface Card](selecting-a-network-interface-card.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="41e01-122">Требования</span><span class="sxs-lookup"><span data-stu-id="41e01-122">Requirements</span></span>



| <span data-ttu-id="41e01-123">Требование</span><span class="sxs-lookup"><span data-stu-id="41e01-123">Requirement</span></span> | <span data-ttu-id="41e01-124">Значение</span><span class="sxs-lookup"><span data-stu-id="41e01-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41e01-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41e01-125">Minimum supported client</span></span><br/> | <span data-ttu-id="41e01-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="41e01-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="41e01-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41e01-127">Minimum supported server</span></span><br/> | <span data-ttu-id="41e01-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="41e01-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="41e01-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="41e01-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="41e01-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="41e01-130"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="41e01-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="41e01-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="41e01-132"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41e01-132"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="41e01-133">DLL</span><span class="sxs-lookup"><span data-stu-id="41e01-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41e01-134"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41e01-134"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41e01-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41e01-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41e01-136">жетнппблобфромуи</span><span class="sxs-lookup"><span data-stu-id="41e01-136">GetNPPBlobFromUI</span></span>](getnppblobfromui.md)
</dt> <dt>

[<span data-ttu-id="41e01-137">жетнппблобтабле</span><span class="sxs-lookup"><span data-stu-id="41e01-137">GetNPPBlobTable</span></span>](getnppblobtable.md)
</dt> <dt>

[<span data-ttu-id="41e01-138">Специальные записи BLOB-объектов</span><span class="sxs-lookup"><span data-stu-id="41e01-138">Special BLOB Entries</span></span>](special-blob-entries.md)
</dt> </dl>

 

 




