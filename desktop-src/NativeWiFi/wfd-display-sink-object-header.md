---
description: Описывает данные объекта отображаемого приемника, входящие в уведомление или результат уведомления.
ms.assetid: 40D931F6-C068-48EB-A968-9CBAA3F9FAD8
title: Структура WFD_DISPLAY_SINK_OBJECT_HEADER (Вфдсинк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: cdefd6b0b91fefb0f42a6e37e7584f7cd966884b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909427"
---
# <a name="wfd_display_sink_object_header-structure"></a><span data-ttu-id="8dc6e-103">\_ \_ \_ Структура заголовка объекта приемника WFD \_</span><span class="sxs-lookup"><span data-stu-id="8dc6e-103">WFD\_DISPLAY\_SINK\_OBJECT\_HEADER structure</span></span>

<span data-ttu-id="8dc6e-104">Структура **\_ \_ \_ \_ заголовка объекта для приемника WFD** описывает данные объекта приемника, входящие в уведомление или результат уведомления.</span><span class="sxs-lookup"><span data-stu-id="8dc6e-104">The **WFD\_DISPLAY\_SINK\_OBJECT\_HEADER** structure describes the display sink object data included in a notification or notification result.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dc6e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8dc6e-105">Syntax</span></span>


```C++
typedef struct _WFD_DISPLAY_SINK_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Length;
} WFD_DISPLAY_SINK_OBJECT_HEADER, *PWFD_DISPLAY_SINK_OBJECT_HEADER;
```



## <a name="members"></a><span data-ttu-id="8dc6e-106">Члены</span><span class="sxs-lookup"><span data-stu-id="8dc6e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8dc6e-107">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8dc6e-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="8dc6e-108">Тип объекта приемника дисплея.</span><span class="sxs-lookup"><span data-stu-id="8dc6e-108">The type of the display sink object.</span></span> <span data-ttu-id="8dc6e-109">Можно использовать идентификатор **\_ \_ типа объекта приемника WFD \_ \_ \_ по умолчанию** , который определен как значение 1.</span><span class="sxs-lookup"><span data-stu-id="8dc6e-109">You can use the identifier **WFD\_DISPLAY\_SINK\_OBJECT\_TYPE\_DEFAULT** which is defined as the value 1.</span></span>

</dd> <dt>

<span data-ttu-id="8dc6e-110">**Редакции**</span><span class="sxs-lookup"><span data-stu-id="8dc6e-110">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="8dc6e-111">Версия редакции объекта приемника экрана.</span><span class="sxs-lookup"><span data-stu-id="8dc6e-111">The revision version of the display sink object.</span></span> <span data-ttu-id="8dc6e-112">Можно использовать идентификатор WFD, **\_ \_ \_ \_ редакция \_ \_ 1 объекта приемника** , который определен как значение 1.</span><span class="sxs-lookup"><span data-stu-id="8dc6e-112">You can use the identifier **WFD\_DISPLAY\_SINK\_OBJECT\_REVISION\_VERSION\_1** which is defined as the value 1.</span></span>

</dd> <dt>

<span data-ttu-id="8dc6e-113">**Длина**</span><span class="sxs-lookup"><span data-stu-id="8dc6e-113">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="8dc6e-114">Длина данных в уведомлении или в результатах уведомления.</span><span class="sxs-lookup"><span data-stu-id="8dc6e-114">The length of the data in the notification or notification result.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8dc6e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8dc6e-115">Requirements</span></span>



| <span data-ttu-id="8dc6e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8dc6e-116">Requirement</span></span> | <span data-ttu-id="8dc6e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8dc6e-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8dc6e-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8dc6e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8dc6e-119">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8dc6e-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8dc6e-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8dc6e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8dc6e-121">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8dc6e-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8dc6e-122">Header</span><span class="sxs-lookup"><span data-stu-id="8dc6e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dc6e-123"><dt>Вфдсинк. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dc6e-123"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




