---
description: Записывает двоичные данные в указанную базу данных.
ms.assetid: 935321b8-904e-46be-ad11-77d89670a072
title: Функция Сдбвритебинаритаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e79de8549eb4c0a0f1b8a914c59d21ccfb3bcf7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538645"
---
# <a name="sdbwritebinarytag-function"></a><span data-ttu-id="134c0-103">Функция Сдбвритебинаритаг</span><span class="sxs-lookup"><span data-stu-id="134c0-103">SdbWriteBinaryTag function</span></span>

<span data-ttu-id="134c0-104">Записывает двоичные данные в указанную базу данных.</span><span class="sxs-lookup"><span data-stu-id="134c0-104">Writes binary data to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="134c0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="134c0-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteBinaryTag(
  _In_ PDB   pdb,
  _In_ TAG   tTag,
  _In_ PBYTE pBuffer,
  _In_ DWORD dwSize
);
```



## <a name="parameters"></a><span data-ttu-id="134c0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="134c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="134c0-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="134c0-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="134c0-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="134c0-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="134c0-109">*ттаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="134c0-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="134c0-110">ТЕГ для записи.</span><span class="sxs-lookup"><span data-stu-id="134c0-110">The TAG for the entry.</span></span> <span data-ttu-id="134c0-111">Этот тег должен иметь тип **\_ \_ binary типа Tag**.</span><span class="sxs-lookup"><span data-stu-id="134c0-111">This TAG must be of type **TAG\_TYPE\_BINARY**.</span></span>

</dd> <dt>

<span data-ttu-id="134c0-112">*pBuffer* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="134c0-112">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="134c0-113">Буфер, содержащий данные.</span><span class="sxs-lookup"><span data-stu-id="134c0-113">The buffer that contains the data.</span></span> <span data-ttu-id="134c0-114">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="134c0-114">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="134c0-115">*двсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="134c0-115">*dwSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="134c0-116">Размер буфера *pBuffer* в байтах.</span><span class="sxs-lookup"><span data-stu-id="134c0-116">The size of the *pBuffer* buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="134c0-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="134c0-117">Return value</span></span>

<span data-ttu-id="134c0-118">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="134c0-118">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="134c0-119">Требования</span><span class="sxs-lookup"><span data-stu-id="134c0-119">Requirements</span></span>



| <span data-ttu-id="134c0-120">Требование</span><span class="sxs-lookup"><span data-stu-id="134c0-120">Requirement</span></span> | <span data-ttu-id="134c0-121">Значение</span><span class="sxs-lookup"><span data-stu-id="134c0-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="134c0-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="134c0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="134c0-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="134c0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="134c0-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="134c0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="134c0-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="134c0-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="134c0-126">DLL</span><span class="sxs-lookup"><span data-stu-id="134c0-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="134c0-127"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="134c0-127"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="134c0-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="134c0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="134c0-129">**сдбвритебинаритагфромфиле**</span><span class="sxs-lookup"><span data-stu-id="134c0-129">**SdbWriteBinaryTagFromFile**</span></span>](sdbwritebinarytagfromfile.md)
</dt> <dt>

[<span data-ttu-id="134c0-130">**сдбвритедвордтаг**</span><span class="sxs-lookup"><span data-stu-id="134c0-130">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="134c0-131">**сдбвритеквордтаг**</span><span class="sxs-lookup"><span data-stu-id="134c0-131">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="134c0-132">**сдбвритестрингтаг**</span><span class="sxs-lookup"><span data-stu-id="134c0-132">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="134c0-133">**сдбвритевордтаг**</span><span class="sxs-lookup"><span data-stu-id="134c0-133">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




