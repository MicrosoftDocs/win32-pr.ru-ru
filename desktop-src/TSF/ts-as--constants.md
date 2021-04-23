---
title: Константы TS_AS_ (Текстстор. h)
description: Следующие флаги задают события, вызывающие методы AdviseSink.
ms.assetid: 8f406b67-f846-4712-b4be-811dbcc6ad55
topic_type:
- apiref
api_name:
- TS_AS_TEXT_CHANGE
- TS_AS_SEL_CHANGE
- TS_AS_LAYOUT_CHANGE
- TS_AS_ATTR_CHANGE
- TS_AS_STATUS_CHANGE
- TS_AS_ALL_SINKS
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c7b36bdc2c3b559693503b2a8e408a0782855f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682037"
---
# <a name="ts_as_-constants"></a><span data-ttu-id="71922-103">TS \_ в качестве \_ \* констант</span><span class="sxs-lookup"><span data-stu-id="71922-103">TS\_AS\_\* Constants</span></span>

<span data-ttu-id="71922-104">Следующие флаги задают события, вызывающие методы **AdviseSink** .</span><span class="sxs-lookup"><span data-stu-id="71922-104">The following flags specify the events that call the **AdviseSink** methods.</span></span>



| <span data-ttu-id="71922-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="71922-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="71922-106">Описание</span><span class="sxs-lookup"><span data-stu-id="71922-106">Description</span></span>                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="TS_AS_TEXT_CHANGE"></span><span id="ts_as_text_change"></span><dl> <span data-ttu-id="71922-107"><dt>**TS \_ \_ \_ Изменение текста**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="71922-107"><dt>**TS\_AS\_TEXT\_CHANGE**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                                                                                               | <span data-ttu-id="71922-108">В документе изменяется текст.</span><span class="sxs-lookup"><span data-stu-id="71922-108">Text is changed in the document.</span></span><br/>                          |
| <span id="TS_AS_SEL_CHANGE"></span><span id="ts_as_sel_change"></span><dl> <span data-ttu-id="71922-109"><dt>**TS \_ \_ \_ Изменение SEL**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="71922-109"><dt>**TS\_AS\_SEL\_CHANGE**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                                                                                                  | <span data-ttu-id="71922-110">Текст, выделенный в документе.</span><span class="sxs-lookup"><span data-stu-id="71922-110">Text is selected in the document.</span></span><br/>                         |
| <span id="TS_AS_LAYOUT_CHANGE"></span><span id="ts_as_layout_change"></span><dl> <span data-ttu-id="71922-111"><dt>**TS \_ \_ \_ Изменение макета**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="71922-111"><dt>**TS\_AS\_LAYOUT\_CHANGE**</dt> <dt>( 0x4 )</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="71922-112">Изменяется макет документа.</span><span class="sxs-lookup"><span data-stu-id="71922-112">The layout of the document is changed.</span></span><br/>                    |
| <span id="TS_AS_ATTR_CHANGE"></span><span id="ts_as_attr_change"></span><dl> <span data-ttu-id="71922-113"><dt>**TS \_ КАК \_ \_ изменение attr**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="71922-113"><dt>**TS\_AS\_ATTR\_CHANGE**</dt> <dt>( 0x8 )</dt></span></span> </dl>                                                                                                               | <span data-ttu-id="71922-114">Атрибуты документа изменяются.</span><span class="sxs-lookup"><span data-stu-id="71922-114">The attributes of the document is changed.</span></span><br/>                |
| <span id="TS_AS_STATUS_CHANGE"></span><span id="ts_as_status_change"></span><dl> <span data-ttu-id="71922-115"><dt>**TS \_ При \_ \_ изменении состояния**</dt> <dt>(0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="71922-115"><dt>**TS\_AS\_STATUS\_CHANGE**</dt> <dt>( 0x10 )</dt></span></span> </dl>                                                                                                        | <span data-ttu-id="71922-116">Изменилось состояние документа.</span><span class="sxs-lookup"><span data-stu-id="71922-116">The status of the document is changed.</span></span><br/>                    |
| <span id="TS_AS_ALL_SINKS"></span><span id="ts_as_all_sinks"></span><dl> <span data-ttu-id="71922-117"><dt>**TS \_ так как \_ все \_ приемники**</dt> <dt>(TS \_ As \_ Text меняют TS как SEL меняют состояние TS как attr изменяют TS при изменении \_ \| \_ \_ \_ \| \_ \_ \_ \| \_ \_ \_ \| \_ \_ состояния \_ )</dt></span><span class="sxs-lookup"><span data-stu-id="71922-117"><dt>**TS\_AS\_ALL\_SINKS**</dt> <dt>( TS\_AS\_TEXT\_CHANGE \| TS\_AS\_SEL\_CHANGE \| TS\_AS\_LAYOUT\_CHANGE \| TS\_AS\_ATTR\_CHANGE \| TS\_AS\_STATUS\_CHANGE )</dt></span></span> </dl> | <span data-ttu-id="71922-118">Одно из предыдущих четырех событий, произошедших в документе.</span><span class="sxs-lookup"><span data-stu-id="71922-118">One of the previous four events occurred in the document.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="71922-119">Требования</span><span class="sxs-lookup"><span data-stu-id="71922-119">Requirements</span></span>



| <span data-ttu-id="71922-120">Требование</span><span class="sxs-lookup"><span data-stu-id="71922-120">Requirement</span></span> | <span data-ttu-id="71922-121">Значение</span><span class="sxs-lookup"><span data-stu-id="71922-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71922-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71922-122">Minimum supported client</span></span><br/> | <span data-ttu-id="71922-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="71922-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="71922-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71922-124">Minimum supported server</span></span><br/> | <span data-ttu-id="71922-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="71922-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="71922-126">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="71922-126">Redistributable</span></span><br/>          | <span data-ttu-id="71922-127">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="71922-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="71922-128">Header</span><span class="sxs-lookup"><span data-stu-id="71922-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="71922-129"><dt>Текстстор. h</dt></span><span class="sxs-lookup"><span data-stu-id="71922-129"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="71922-130">IDL</span><span class="sxs-lookup"><span data-stu-id="71922-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="71922-131"><dt>Текстстор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="71922-131"><dt>Textstor.idl</dt></span></span> </dl> |



 

 





