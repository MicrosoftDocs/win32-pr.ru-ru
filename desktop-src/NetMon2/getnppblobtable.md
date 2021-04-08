---
description: Функция Жетнппблобтабле извлекает таблицу больших двоичных объектов НПП, представляющую сетевые карты ККМ на локальном компьютере.
ms.assetid: 9e61faf5-1f06-40b5-bf47-f258ffb5151a
title: Функция Жетнппблобтабле (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 883493215aaac0fa2568baec69232b379b8aa808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910884"
---
# <a name="getnppblobtable-function"></a><span data-ttu-id="bf558-103">Функция Жетнппблобтабле</span><span class="sxs-lookup"><span data-stu-id="bf558-103">GetNPPBlobTable function</span></span>

<span data-ttu-id="bf558-104">Функция **жетнппблобтабле** извлекает таблицу больших двоичных объектов НПП, представляющую сетевые карты ККМ на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="bf558-104">The **GetNPPBlobTable** function retrieves an NPP BLOB table that represents the register NICs on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf558-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf558-105">Syntax</span></span>


```C++
DWORD GetNPPBlobTable(
  _In_  HBLOB       hFilterBlob,
  _Out_ PBLOB_TABLE *ppBlobTable
);
```



## <a name="parameters"></a><span data-ttu-id="bf558-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf558-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf558-107">*хфилтерблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf558-107">*hFilterBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf558-108">Маркер для фильтра BLOB, ограничивающий большие двоичные объекты НПП, возвращаемые в таблице.</span><span class="sxs-lookup"><span data-stu-id="bf558-108">Handle to a filter BLOB that limits the NPP BLOBs returned in the table.</span></span>

</dd> <dt>

<span data-ttu-id="bf558-109">*ппблобтабле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bf558-109">*ppBlobTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf558-110">Указатель на структуру [ \_ таблицы больших двоичных объектов](blob-table.md) , содержащую по крайней мере один указатель BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="bf558-110">Pointer to a [BLOB\_TABLE](blob-table.md) structure that contains at least one BLOB pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf558-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf558-111">Return value</span></span>

<span data-ttu-id="bf558-112">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="bf558-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="bf558-113">Если функция не выполнена, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="bf558-113">If the function is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="bf558-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bf558-114">Return code</span></span>                                                                                                | <span data-ttu-id="bf558-115">Описание</span><span class="sxs-lookup"><span data-stu-id="bf558-115">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bf558-116"><dt>**НМЕРР \_ нет \_ \_ библиотеки DLL НПП**</dt></span><span class="sxs-lookup"><span data-stu-id="bf558-116"><dt>**NMERR\_NO\_NPP\_DLL**</dt></span></span> </dl>         | <span data-ttu-id="bf558-117">В каталоге НПП не найдены библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="bf558-117">No DLLs were found in the NPP directory.</span></span><br/>                    |
| <dl> <span data-ttu-id="bf558-118"><dt>**НМЕРР \_ нет \_ допустимых \_ \_ библиотек DLL НПП**</dt></span><span class="sxs-lookup"><span data-stu-id="bf558-118"><dt>**NMERR\_NO\_VALID\_NPP\_DLLS**</dt></span></span> </dl> | <span data-ttu-id="bf558-119">Ни одна из библиотек DLL в каталоге НПП не была допустимой библиотекой DLL НПП.</span><span class="sxs-lookup"><span data-stu-id="bf558-119">None of the DLLs in the NPP directory were valid NPP DLLs.</span></span><br/>  |
| <dl> <span data-ttu-id="bf558-120"><dt>**НМЕРР \_ без \_ соответствующего \_ НППС**</dt></span><span class="sxs-lookup"><span data-stu-id="bf558-120"><dt>**NMERR\_NO\_MATCHING\_NPPS**</dt></span></span> </dl>   | <span data-ttu-id="bf558-121">Обнаружены большие двоичные объекты НПП, но проверка фильтра не пройдена.</span><span class="sxs-lookup"><span data-stu-id="bf558-121">NPP BLOBs were discovered, but none passed the filter test.</span></span><br/> |
| <dl> <span data-ttu-id="bf558-122"><dt>**НМЕРР \_ из \_ поля \_ MEMO**</dt></span><span class="sxs-lookup"><span data-stu-id="bf558-122"><dt>**NMERR\_OUT\_OF\_MEMOR**</dt></span></span> </dl>       | <span data-ttu-id="bf558-123">Сетевой монитор не удалось выделить память.</span><span class="sxs-lookup"><span data-stu-id="bf558-123">Network Monitor was not able to allocate memory.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="bf558-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf558-124">Remarks</span></span>

<span data-ttu-id="bf558-125">Большой двоичный объект с именем *хфилтерблоб* также может быть специальным BLOB-объектом.</span><span class="sxs-lookup"><span data-stu-id="bf558-125">The BLOB named by *hFilterBlob* can also be a special BLOB.</span></span>

<span data-ttu-id="bf558-126">Если установить флаг в поле Фильтровать большой двоичный объект в **значение true**, то возвращаемая таблица больших двоичных объектов также может содержать специальные большие двоичные объекты.</span><span class="sxs-lookup"><span data-stu-id="bf558-126">If you set the flag in the filter BLOB to **TRUE**, the returned BLOB table can also include special BLOBs .</span></span>

<span data-ttu-id="bf558-127">Если большой двоичный объект с именем *хфилтерблоб* является специальным BLOB-объектом, сетевой монитор пользовательский интерфейс попытается обработать его.</span><span class="sxs-lookup"><span data-stu-id="bf558-127">If the BLOB named by *hFilterBlob* is a special BLOB, the Network Monitor UI will attempt to process it.</span></span> <span data-ttu-id="bf558-128">Например, предположим, что предыдущий вызов возвращает специальный большой двоичный объект из удаленного НПП.</span><span class="sxs-lookup"><span data-stu-id="bf558-128">For example, suppose that a previous call returns a special BLOB from the remote NPP.</span></span> <span data-ttu-id="bf558-129">Приложение вставит требуемый тег, имя компьютера \_ .</span><span class="sxs-lookup"><span data-stu-id="bf558-129">The application inserts the required tag, MACHINE\_NAME.</span></span> <span data-ttu-id="bf558-130">Затем метод поиска передает этот большой двоичный объект удаленному НПП, который затем возвращает таблицу больших двоичных объектов НПП, связанных с именем компьютера.</span><span class="sxs-lookup"><span data-stu-id="bf558-130">The finder then passes this BLOB to the remote NPP, which then returns a table of the NPP BLOBs associated with the machine name.</span></span>

<span data-ttu-id="bf558-131">Для уничтожения всех возвращенных больших двоичных объектов и таблицы больших двоичных объектов вызывающий объект отвечает за вызов функции **дестройблоб** .</span><span class="sxs-lookup"><span data-stu-id="bf558-131">To destroy all returned BLOBs and the BLOB table, the caller is responsible for calling the **DestroyBlob** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf558-132">Требования</span><span class="sxs-lookup"><span data-stu-id="bf558-132">Requirements</span></span>



| <span data-ttu-id="bf558-133">Требование</span><span class="sxs-lookup"><span data-stu-id="bf558-133">Requirement</span></span> | <span data-ttu-id="bf558-134">Значение</span><span class="sxs-lookup"><span data-stu-id="bf558-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf558-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bf558-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bf558-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bf558-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bf558-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bf558-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bf558-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bf558-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bf558-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bf558-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf558-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf558-140"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="bf558-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bf558-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="bf558-142"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf558-142"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="bf558-143">DLL</span><span class="sxs-lookup"><span data-stu-id="bf558-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf558-144"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf558-144"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




