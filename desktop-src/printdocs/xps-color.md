---
description: Структура, описывающая одно значение цвета.
ms.assetid: 710f3ef1-bbc3-416d-9faf-aa4a716007c2
title: XPS_COLOR (Кспсобжектмодел. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34c148c2a5452154bfe33b0c74d695fe78f0cdad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712699"
---
# <a name="xps_color"></a><span data-ttu-id="3a713-103">\_Цвет XPS</span><span class="sxs-lookup"><span data-stu-id="3a713-103">XPS\_COLOR</span></span>

<span data-ttu-id="3a713-104">Структура, описывающая одно значение цвета.</span><span class="sxs-lookup"><span data-stu-id="3a713-104">A structure that describes a single color value.</span></span>

``` syntax
typedef union switch (XPS_COLOR_TYPE colorType) value
{
    case XPS_COLOR_TYPE_SRGB:
        struct {
            byte alpha, red, green, blue;
        } sRGB;
    case XPS_COLOR_TYPE_SCRGB:
        struct {
            FLOAT alpha, red, green, blue;
        } scRGB;
    case XPS_COLOR_TYPE_CONTEXT:
        struct {
            byte channelCount;
            FLOAT channels[9];
        } context;
} XPS_COLOR;
```

## <a name="remarks"></a><span data-ttu-id="3a713-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a713-105">Remarks</span></span>

<span data-ttu-id="3a713-106">Формат структуры зависит от значения *колортипе*.</span><span class="sxs-lookup"><span data-stu-id="3a713-106">The structure's format depends on the value of *colorType*.</span></span>

<dl>

<span data-ttu-id="3a713-107">[**\_Тип цвета \_ XPS \_ sRGB**](/previous-versions/windows/desktop/dd372944(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3a713-107">[**XPS\_COLOR\_TYPE\_SRGB**](/previous-versions/windows/desktop/dd372944(v=vs.85))</span></span>  
<span data-ttu-id="3a713-108">[**\_Тип цвета \_ XPS \_ SCRGB**](/previous-versions/windows/desktop/dd372943(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3a713-108">[**XPS\_COLOR\_TYPE\_SCRGB**](/previous-versions/windows/desktop/dd372943(v=vs.85))</span></span>  
[<span data-ttu-id="3a713-109">**\_ \_ контекст типа цвета \_ XPS**</span><span class="sxs-lookup"><span data-stu-id="3a713-109">**XPS\_COLOR\_TYPE\_CONTEXT**</span></span>](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color)  
</dl>

## <a name="requirements"></a><span data-ttu-id="3a713-110">Требования</span><span class="sxs-lookup"><span data-stu-id="3a713-110">Requirements</span></span>



| <span data-ttu-id="3a713-111">Требование</span><span class="sxs-lookup"><span data-stu-id="3a713-111">Requirement</span></span> | <span data-ttu-id="3a713-112">Значение</span><span class="sxs-lookup"><span data-stu-id="3a713-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a713-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a713-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3a713-114">Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для \[ классических приложений Windows Vista \| приложения UWP\]</span><span class="sxs-lookup"><span data-stu-id="3a713-114">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="3a713-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a713-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3a713-116">Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 классические \[ приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3a713-116">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="3a713-117">Header</span><span class="sxs-lookup"><span data-stu-id="3a713-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a713-118"><dt>Кспсобжектмодел. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a713-118"><dt>Xpsobjectmodel.h</dt></span></span> </dl>                                              |
| <span data-ttu-id="3a713-119">IDL</span><span class="sxs-lookup"><span data-stu-id="3a713-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3a713-120"><dt>Кспсобжектмодел. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3a713-120"><dt>XpsObjectModel.idl</dt></span></span> </dl>                                            |



## <a name="see-also"></a><span data-ttu-id="3a713-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a713-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a713-122">XPS</span><span class="sxs-lookup"><span data-stu-id="3a713-122">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

