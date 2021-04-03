---
description: Выбирает регистрацию сетевого адаптера.
ms.assetid: 27814a40-6933-498b-a0d2-535698b1e402
title: Функция Жетнппблобфромуи (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobFromUI
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 4ff3887f10d35ec3b66d8eaaf1443140c768ca55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998783"
---
# <a name="getnppblobfromui-function"></a><span data-ttu-id="649d4-103">Функция Жетнппблобфромуи</span><span class="sxs-lookup"><span data-stu-id="649d4-103">GetNPPBlobFromUI function</span></span>

<span data-ttu-id="649d4-104">Функция **жетнппблобфромуи** выбирает регистрацию сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="649d4-104">The **GetNPPBlobFromUI** function selects a register NIC.</span></span>

## <a name="syntax"></a><span data-ttu-id="649d4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="649d4-105">Syntax</span></span>


```C++
DWORD GetNPPBlobFromUI(
  _In_  HWND  hwnd,
  _In_  HBLOB hFilterBlob,
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a><span data-ttu-id="649d4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="649d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="649d4-107">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="649d4-107">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="649d4-108">Маркер окна, отображающего диалоговое окно **Выбор сети** .</span><span class="sxs-lookup"><span data-stu-id="649d4-108">A handle to a window that displays the **Select a network** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="649d4-109">*хфилтерблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="649d4-109">*hFilterBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="649d4-110">Маркер для [*фильтра BLOB*](f.md) , используемый для ограничения отображаемых сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="649d4-110">A handle to a [*filter BLOB*](f.md) used to limit which NICs are displayed.</span></span>

</dd> <dt>

<span data-ttu-id="649d4-111">*фблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="649d4-111">*phBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="649d4-112">Указатель на маркер большого двоичного объекта, представляющий выбранную сетевую карту.</span><span class="sxs-lookup"><span data-stu-id="649d4-112">A pointer to the handle of the BLOB that represents the selected NIC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="649d4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="649d4-113">Return value</span></span>

<span data-ttu-id="649d4-114">Если функция выполнена успешно (пользователь выбирает сетевую карту), возвращаемое значение — НМЕРР \_ Success, а BLOB-объект, на который указывает *фблоб* , заполнен.</span><span class="sxs-lookup"><span data-stu-id="649d4-114">If the function is successful (the user selects a NIC), the return value is NMERR\_SUCCESS, and the BLOB that *phBlob* points to is filled in.</span></span>

<span data-ttu-id="649d4-115">Если пользователь не выбрал сетевую карту, возвращается значение **нмерр \_ No \_ НПП \_**.</span><span class="sxs-lookup"><span data-stu-id="649d4-115">If the user does not select an NIC, the return value is **NMERR\_NO\_NPP\_SELECTED**.</span></span>

<span data-ttu-id="649d4-116">Если функция завершается неудачно, возвращается значение другого НМЕРР.</span><span class="sxs-lookup"><span data-stu-id="649d4-116">If the function is unsuccessful, the return value is another NMERR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="649d4-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="649d4-117">Remarks</span></span>

<span data-ttu-id="649d4-118">При вызове сетевой монитор отображает диалоговое окно **Выбор сети** , которое можно использовать для выбора сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="649d4-118">When called, Network Monitor displays the **Select a network** dialog box, which you can use to select a NIC.</span></span> <span data-ttu-id="649d4-119">Большой двоичный объект НПП, представляющий сетевую карту, возвращается вызывающему приложению.</span><span class="sxs-lookup"><span data-stu-id="649d4-119">The NPP BLOB that represents the NIC is returned to the calling application.</span></span>

<span data-ttu-id="649d4-120">Если большой двоичный объект с именем *хфилтерблоб* является [*специальным BLOB-объектом*](s.md), он попытается обработать его.</span><span class="sxs-lookup"><span data-stu-id="649d4-120">If the BLOB named by *hFilterBlob* is a [*special BLOB*](s.md), the finder will attempt to process it.</span></span> <span data-ttu-id="649d4-121">В качестве примера можно привести вызов, который ранее возвращал Специальный большой двоичный объект из удаленного НПП.</span><span class="sxs-lookup"><span data-stu-id="649d4-121">An example would be a call that had previously returned a special BLOB from the remote NPP.</span></span> <span data-ttu-id="649d4-122">Приложение вставило требуемый тег, \_ имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="649d4-122">The application inserted the required tag, MACHINE\_NAME.</span></span> <span data-ttu-id="649d4-123">В этом случае Finder передает этот большой двоичный объект удаленному НПП, который затем возвращает таблицу из НПП BLOB-объектов, представляющих запрошенный компьютер.</span><span class="sxs-lookup"><span data-stu-id="649d4-123">In this situation, the finder would pass this BLOB to the remote NPP, which would then return a table of NPP BLOBs representing the machine requested.</span></span> <span data-ttu-id="649d4-124">Эти удаленные BLOB-объекты НПП будут отображаться в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="649d4-124">These remote NPP BLOBs would appear in the dialog box.</span></span>

<span data-ttu-id="649d4-125">Вызывающий объект должен вызвать функцию [дестройблоб](destroyblob.md) , которая уничтожает ВОЗВРАЩЕННЫЙ большой двоичный объект, когда он больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="649d4-125">The caller must call the [DestroyBlob](destroyblob.md) function, which destroys the returned BLOB when it is no longer required.</span></span>



| <span data-ttu-id="649d4-126">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="649d4-126">For more information about</span></span> | <span data-ttu-id="649d4-127">См.</span><span class="sxs-lookup"><span data-stu-id="649d4-127">See</span></span>                                                                          |
|----------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="649d4-128">Три способа выбора сетевых карт</span><span class="sxs-lookup"><span data-stu-id="649d4-128">Three ways to select NICs</span></span>  | [<span data-ttu-id="649d4-129">Выбор сетевой карты</span><span class="sxs-lookup"><span data-stu-id="649d4-129">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |
| <span data-ttu-id="649d4-130">Указание фильтра BLOB</span><span class="sxs-lookup"><span data-stu-id="649d4-130">Specifying a filter BLOB</span></span>   | [<span data-ttu-id="649d4-131">Указание фильтра BLOB</span><span class="sxs-lookup"><span data-stu-id="649d4-131">Specifying a Filter BLOB</span></span>](specifying-a-filter-blob.md)                     |



 

## <a name="requirements"></a><span data-ttu-id="649d4-132">Требования</span><span class="sxs-lookup"><span data-stu-id="649d4-132">Requirements</span></span>



| <span data-ttu-id="649d4-133">Требование</span><span class="sxs-lookup"><span data-stu-id="649d4-133">Requirement</span></span> | <span data-ttu-id="649d4-134">Значение</span><span class="sxs-lookup"><span data-stu-id="649d4-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="649d4-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="649d4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="649d4-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="649d4-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="649d4-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="649d4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="649d4-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="649d4-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="649d4-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="649d4-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="649d4-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="649d4-140"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="649d4-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="649d4-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="649d4-142"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="649d4-142"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="649d4-143">DLL</span><span class="sxs-lookup"><span data-stu-id="649d4-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="649d4-144"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="649d4-144"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="649d4-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="649d4-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="649d4-146">жетнппблобтабле</span><span class="sxs-lookup"><span data-stu-id="649d4-146">GetNPPBlobTable</span></span>](getnppblobtable.md)
</dt> <dt>

[<span data-ttu-id="649d4-147">селектнппблобфромтабле</span><span class="sxs-lookup"><span data-stu-id="649d4-147">SelectNPPBlobFromTable</span></span>](selectnppblobfromtable.md)
</dt> </dl>

 

 




