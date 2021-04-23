---
title: Константы ПИКТИПЕ (Олектл. h)
description: Опишите тип объекта изображения, возвращаемый типом Ипиктуре Get \_ , а также описание типа изображения в элементе пиктипе структуры пиктдеск, которая передается олекреатепиктуреиндирект.
ms.assetid: 79f10687-f0eb-4b5e-a1a9-9186dbd0b51f
topic_type:
- apiref
api_name:
- PICTYPE_UNINITIALIZED
- PICTYPE_NONE
- PICTYPE_BITMAP
- PICTYPE_METAFILE
- PICTYPE_ICON
- PICTYPE_ENHMETAFILE
api_location:
- OleCtl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bebf8ad8f678e9b6e463ade9f149b2e1d4bab529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691794"
---
# <a name="pictype-constants"></a><span data-ttu-id="186ff-103">Константы ПИКТИПЕ</span><span class="sxs-lookup"><span data-stu-id="186ff-103">PICTYPE Constants</span></span>

<span data-ttu-id="186ff-104">Опишите тип объекта изображения, возвращаемый функцией [**ипиктуре:: Get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type), а также описание типа изображения в элементе **пиктипе** структуры [**пиктдеск**](/windows/win32/api/olectl/ns-olectl-pictdesc) , передаваемой [**олекреатепиктуреиндирект**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span><span class="sxs-lookup"><span data-stu-id="186ff-104">Describe the type of a picture object as returned by [**IPicture::get\_Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type), as well as to describe the type of picture in the **picType** member of the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure that is passed to [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span></span>



| <span data-ttu-id="186ff-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="186ff-105">Constant/value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="186ff-106">Описание</span><span class="sxs-lookup"><span data-stu-id="186ff-106">Description</span></span>                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PICTYPE_UNINITIALIZED"></span><span id="pictype_uninitialized"></span><dl> <span data-ttu-id="186ff-107"><dt>**Пиктипе \_ Не ИНИЦИАЛИЗИРОВАНо**</dt> <dt>(-1)</dt></span><span class="sxs-lookup"><span data-stu-id="186ff-107"><dt>**PICTYPE\_UNINITIALIZED**</dt> <dt>(-1)</dt></span></span> </dl> | <span data-ttu-id="186ff-108">Объект изображения в настоящее время не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="186ff-108">The picture object is currently uninitialized.</span></span> <span data-ttu-id="186ff-109">Это значение допустимо только в качестве возвращаемого значения из [**ипиктуре:: Get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) и недопустимо для структуры [**пиктдеск**](/windows/win32/api/olectl/ns-olectl-pictdesc) .</span><span class="sxs-lookup"><span data-stu-id="186ff-109">This value is only valid as a return value from [**IPicture::get\_Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) and is not valid with the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure.</span></span><br/>  |
| <span id="PICTYPE_NONE"></span><span id="pictype_none"></span><dl> <span data-ttu-id="186ff-110"><dt>**Пиктипе \_ НЕТ**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="186ff-110"><dt>**PICTYPE\_NONE**</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="186ff-111">Новый объект изображения будет создан без инициализированного состояния.</span><span class="sxs-lookup"><span data-stu-id="186ff-111">A new picture object is to be created without an initialized state.</span></span> <span data-ttu-id="186ff-112">Это значение допустимо только в структуре [**пиктдеск**](/windows/win32/api/olectl/ns-olectl-pictdesc) .</span><span class="sxs-lookup"><span data-stu-id="186ff-112">This value is valid only in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure.</span></span><br/>                                                                        |
| <span id="PICTYPE_BITMAP"></span><span id="pictype_bitmap"></span><dl> <span data-ttu-id="186ff-113"><dt>**Пиктипе \_ ТОЧЕЧный рисунок**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="186ff-113"><dt>**PICTYPE\_BITMAP**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="186ff-114">Тип изображения — точечный рисунок.</span><span class="sxs-lookup"><span data-stu-id="186ff-114">The picture type is a bitmap.</span></span> <span data-ttu-id="186ff-115">Если это значение встречается в структуре [**пиктдеск**](/windows/win32/api/olectl/ns-olectl-pictdesc) , это означает, что поле **BMP** этой структуры содержит соответствующие параметры инициализации.</span><span class="sxs-lookup"><span data-stu-id="186ff-115">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **bmp** field of that structure contains the relevant initialization parameters.</span></span><br/>             |
| <span id="PICTYPE_METAFILE"></span><span id="pictype_metafile"></span><dl> <span data-ttu-id="186ff-116"><dt>**Пиктипе \_ МЕТАФАЙЛ**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="186ff-116"><dt>**PICTYPE\_METAFILE**</dt> <dt>2</dt></span></span> </dl>                   | <span data-ttu-id="186ff-117">Тип изображения — метафайл.</span><span class="sxs-lookup"><span data-stu-id="186ff-117">The picture type is a metafile.</span></span> <span data-ttu-id="186ff-118">Если это значение встречается в структуре [**пиктдеск**](/windows/win32/api/olectl/ns-olectl-pictdesc) , это означает, что поле **WMF** этой структуры содержит соответствующие параметры инициализации.</span><span class="sxs-lookup"><span data-stu-id="186ff-118">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **wmf** field of that structure contains the relevant initialization parameters.</span></span><br/>           |
| <span id="PICTYPE_ICON"></span><span id="pictype_icon"></span><dl> <span data-ttu-id="186ff-119"><dt>**Пиктипе \_ ЗНАЧОК**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="186ff-119"><dt>**PICTYPE\_ICON**</dt> <dt>3</dt></span></span> </dl>                               | <span data-ttu-id="186ff-120">Тип изображения — значок.</span><span class="sxs-lookup"><span data-stu-id="186ff-120">The picture type is an icon.</span></span> <span data-ttu-id="186ff-121">Если это значение встречается в структуре [**пиктдеск**](/windows/win32/api/olectl/ns-olectl-pictdesc) , это означает, что поле **Icon** этой структуры содержит соответствующие параметры инициализации.</span><span class="sxs-lookup"><span data-stu-id="186ff-121">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **icon** field of that structure contains the relevant initialization parameters.</span></span><br/>             |
| <span id="PICTYPE_ENHMETAFILE"></span><span id="pictype_enhmetafile"></span><dl> <span data-ttu-id="186ff-122"><dt>**Пиктипе \_ ЕНХМЕТАФИЛЕ**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="186ff-122"><dt>**PICTYPE\_ENHMETAFILE**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="186ff-123">Тип изображения является расширенным метафайлом.</span><span class="sxs-lookup"><span data-stu-id="186ff-123">The picture type is an enhanced metafile.</span></span> <span data-ttu-id="186ff-124">Если это значение встречается в структуре [**пиктдеск**](/windows/win32/api/olectl/ns-olectl-pictdesc) , это означает, что поле **EMF** этой структуры содержит соответствующие параметры инициализации.</span><span class="sxs-lookup"><span data-stu-id="186ff-124">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **emf** field of that structure contains the relevant initialization parameters.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="186ff-125">Требования</span><span class="sxs-lookup"><span data-stu-id="186ff-125">Requirements</span></span>



| <span data-ttu-id="186ff-126">Требование</span><span class="sxs-lookup"><span data-stu-id="186ff-126">Requirement</span></span> | <span data-ttu-id="186ff-127">Значение</span><span class="sxs-lookup"><span data-stu-id="186ff-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="186ff-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="186ff-128">Minimum supported client</span></span><br/> | <span data-ttu-id="186ff-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="186ff-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="186ff-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="186ff-130">Minimum supported server</span></span><br/> | <span data-ttu-id="186ff-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="186ff-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="186ff-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="186ff-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="186ff-133"><dt>Олектл. h</dt></span><span class="sxs-lookup"><span data-stu-id="186ff-133"><dt>OleCtl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="186ff-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="186ff-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="186ff-135">**Ипиктуре:: Get \_ Type**</span><span class="sxs-lookup"><span data-stu-id="186ff-135">**IPicture::get\_Type**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)
</dt> <dt>

[<span data-ttu-id="186ff-136">**олекреатепиктуреиндирект**</span><span class="sxs-lookup"><span data-stu-id="186ff-136">**OleCreatePictureIndirect**</span></span>](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)
</dt> <dt>

[<span data-ttu-id="186ff-137">**пиктдеск**</span><span class="sxs-lookup"><span data-stu-id="186ff-137">**PICTDESC**</span></span>](/windows/win32/api/olectl/ns-olectl-pictdesc)
</dt> </dl>

 

 





