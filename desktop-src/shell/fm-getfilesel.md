---
description: Отправляется расширением диспетчера файлов для получения сведений о выбранном файле из активного окна диспетчера файлов (в окне каталога или в окне результатов поиска).
title: Сообщение FM_GETFILESEL (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c2b4aac6-165b-4eba-b012-ee7a20481cd3
ms.openlocfilehash: 2da95a39f8e84215640e926ae21a043865223665
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841425"
---
# <a name="fm_getfilesel-message"></a><span data-ttu-id="a46aa-103">\_Сообщение FM жетфилесел</span><span class="sxs-lookup"><span data-stu-id="a46aa-103">FM\_GETFILESEL message</span></span>

<span data-ttu-id="a46aa-104">Отправляется расширением диспетчера файлов для получения сведений о выбранном файле из активного окна диспетчера файлов (в окне каталога или в окне результатов поиска).</span><span class="sxs-lookup"><span data-stu-id="a46aa-104">Sent by a File Manager extension to retrieve information about a selected file from the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="a46aa-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="a46aa-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a46aa-106">*index*</span><span class="sxs-lookup"><span data-stu-id="a46aa-106">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="a46aa-107">Отсчитываемый от нуля индекс выбранного файла для извлечения.</span><span class="sxs-lookup"><span data-stu-id="a46aa-107">The zero-based index of the selected file to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="a46aa-108">*лпфмсгфс*</span><span class="sxs-lookup"><span data-stu-id="a46aa-108">*lpfmsgfs*</span></span> 
</dt> <dd>

<span data-ttu-id="a46aa-109">Адрес структуры [**FMS \_ жетфилесел**](fms-getfilesel.md) , которая получает сведения о выделенном фрагменте.</span><span class="sxs-lookup"><span data-stu-id="a46aa-109">The address of an [**FMS\_GETFILESEL**](fms-getfilesel.md) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a46aa-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a46aa-110">Return value</span></span>

<span data-ttu-id="a46aa-111">Возвращает отсчитываемый от нуля индекс выбранного файла, который был получен.</span><span class="sxs-lookup"><span data-stu-id="a46aa-111">Returns the zero-based index of the selected file that was retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="a46aa-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="a46aa-112">Remarks</span></span>

<span data-ttu-id="a46aa-113">Расширение может использовать сообщение [**FM \_ жетселкаунт**](fm-getselcount.md) для получения числа выбранных файлов.</span><span class="sxs-lookup"><span data-stu-id="a46aa-113">An extension can use the [**FM\_GETSELCOUNT**](fm-getselcount.md) message to retrieve the count of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="a46aa-114">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="a46aa-114">Requirements</span></span>



| <span data-ttu-id="a46aa-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a46aa-115">Requirement</span></span> | <span data-ttu-id="a46aa-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a46aa-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a46aa-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a46aa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a46aa-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a46aa-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="a46aa-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a46aa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a46aa-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a46aa-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a46aa-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a46aa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a46aa-122"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="a46aa-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a46aa-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a46aa-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a46aa-124">**фмекстенсионпрок**</span><span class="sxs-lookup"><span data-stu-id="a46aa-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="a46aa-125">**FM \_ жетфилеселлфн**</span><span class="sxs-lookup"><span data-stu-id="a46aa-125">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="a46aa-126">**FM \_ жетселкаунтлфн**</span><span class="sxs-lookup"><span data-stu-id="a46aa-126">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




