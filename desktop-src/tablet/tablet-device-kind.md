---
description: Указывает тип устройства планшета, например перо, мышь или сенсорно-чувствительный дигитайзер.
ms.assetid: 4cca1e09-99c0-4357-a6ef-159bc8d17d57
title: Перечисление TABLET_DEVICE_KIND
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_DEVICE_KIND
api_type:
- NA
api_location: ''
ms.openlocfilehash: 18f691a2fa909ef28059a4788f4f8b4e184a61ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674392"
---
# <a name="tablet_device_kind-enumeration"></a><span data-ttu-id="f6def-103">\_Перечисление типов планшетных устройств \_</span><span class="sxs-lookup"><span data-stu-id="f6def-103">TABLET\_DEVICE\_KIND enumeration</span></span>

<span data-ttu-id="f6def-104">Указывает тип устройства планшета, например перо, мышь или сенсорно-чувствительный дигитайзер.</span><span class="sxs-lookup"><span data-stu-id="f6def-104">Indicates the type of tablet device such as a pen, mouse or touch sensitive digitizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6def-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6def-105">Syntax</span></span>


```C++
typedef enum _TABLET_DEVICE_KIND { 
  TABLET_DEVICE_MOUSE  = 0,
  TABLET_DEVICE_PEN,
  TABLET_DEVICE_TOUCH
} TABLET_DEVICE_KIND;
```



## <a name="constants"></a><span data-ttu-id="f6def-106">Константы</span><span class="sxs-lookup"><span data-stu-id="f6def-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f6def-107"><span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**мышь ПЛАНШЕТного \_ устройства \_**</span><span class="sxs-lookup"><span data-stu-id="f6def-107"><span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**TABLET\_DEVICE\_MOUSE**</span></span>
</dt> <dd>

<span data-ttu-id="f6def-108">Планшет — это мышь.</span><span class="sxs-lookup"><span data-stu-id="f6def-108">The tablet is a mouse.</span></span> <span data-ttu-id="f6def-109">Сюда входят сенсорные панели, находящиеся на многих ноутбуках.</span><span class="sxs-lookup"><span data-stu-id="f6def-109">This includes touchpads found on many laptop computers.</span></span>

</dd> <dt>

<span data-ttu-id="f6def-110"><span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**перо ПЛАНШЕТного \_ устройства \_**</span><span class="sxs-lookup"><span data-stu-id="f6def-110"><span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**TABLET\_DEVICE\_PEN**</span></span>
</dt> <dd>

<span data-ttu-id="f6def-111">Планшет использует электромагнитное перо и дигитайзер.</span><span class="sxs-lookup"><span data-stu-id="f6def-111">The tablet utilizes an electromagnetic pen and digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="f6def-112"><span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**\_ \_ сенсорный ввод устройств**</span><span class="sxs-lookup"><span data-stu-id="f6def-112"><span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**TABLET\_DEVICE\_TOUCH**</span></span>
</dt> <dd>

<span data-ttu-id="f6def-113">Планшет использует сенсорно-чувствительный дигитайзер.</span><span class="sxs-lookup"><span data-stu-id="f6def-113">The tablet utilizes a touch sensitive digitizer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6def-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f6def-114">Requirements</span></span>



| <span data-ttu-id="f6def-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f6def-115">Requirement</span></span> | <span data-ttu-id="f6def-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f6def-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f6def-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6def-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f6def-118">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f6def-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f6def-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6def-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f6def-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f6def-120">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="f6def-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6def-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6def-122">**Метод ITablet2:: Жетдевицекинд**</span><span class="sxs-lookup"><span data-stu-id="f6def-122">**ITablet2::GetDeviceKind Method**</span></span>](itablet2-getdevicekind.md)
</dt> </dl>

 

 




