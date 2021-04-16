---
title: Перечисление ТИПЕМОДЕ (Софткбдк. h)
description: Элементы перечисления ТИПЕМОДЕ используются для указания режимов типов, доступных для экранной клавиатуры.
ms.assetid: 7db0a4dd-0ee2-455d-aeb8-11cd1249134c
keywords:
- Платформа текстовых служб перечисления ТИПЕМОДЕ
topic_type:
- apiref
api_name:
- TYPEMODE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24054443802d0b8a759841cb6b3fc3cb5d510024
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672559"
---
# <a name="typemode-enumeration"></a><span data-ttu-id="83722-104">Перечисление ТИПЕМОДЕ</span><span class="sxs-lookup"><span data-stu-id="83722-104">TYPEMODE enumeration</span></span>

<span data-ttu-id="83722-105">Элементы перечисления **типемоде** используются для указания режимов типов, доступных для экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="83722-105">Elements of the **TYPEMODE** enumeration are used to specify type modes that are available for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="83722-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83722-106">Syntax</span></span>


```C++
typedef enum tagTYPEMODE { 
  ClickMouse  = 0,
  Hover       = 1,
  Scanning    = 2
} TYPEMODE;
```



## <a name="constants"></a><span data-ttu-id="83722-107">Константы</span><span class="sxs-lookup"><span data-stu-id="83722-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="83722-108"><span id="ClickMouse"></span><span id="clickmouse"></span><span id="CLICKMOUSE"></span>**кликкмаусе**</span><span class="sxs-lookup"><span data-stu-id="83722-108"><span id="ClickMouse"></span><span id="clickmouse"></span><span id="CLICKMOUSE"></span>**ClickMouse**</span></span>
</dt> <dd>

<span data-ttu-id="83722-109">Пользователь может щелкнуть клавиши на экране, чтобы ввести текст.</span><span class="sxs-lookup"><span data-stu-id="83722-109">The user can click the on-screen keys to type text.</span></span>

</dd> <dt>

<span data-ttu-id="83722-110"><span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**Помещении**</span><span class="sxs-lookup"><span data-stu-id="83722-110"><span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**Hover**</span></span>
</dt> <dd>

<span data-ttu-id="83722-111">Пользователь может указать ключ на определенный период времени, и выбранный символ будет введен автоматически.</span><span class="sxs-lookup"><span data-stu-id="83722-111">The user can point to a key for a predefined period of time, and the selected character is typed automatically.</span></span>

</dd> <dt>

<span data-ttu-id="83722-112"><span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**Проверяет**</span><span class="sxs-lookup"><span data-stu-id="83722-112"><span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**Scanning**</span></span>
</dt> <dd>

<span data-ttu-id="83722-113">С помощью экранной клавиатуры постоянно проверяются область ввода и выделяются области, в которых пользователь может нажать сочетание клавиш или выбрать устройство ввода.</span><span class="sxs-lookup"><span data-stu-id="83722-113">The soft keyboard continually scans the input area and highlights regions where the user can press a shortcut key or use a switch-input device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="83722-114">Требования</span><span class="sxs-lookup"><span data-stu-id="83722-114">Requirements</span></span>



| <span data-ttu-id="83722-115">Требование</span><span class="sxs-lookup"><span data-stu-id="83722-115">Requirement</span></span> | <span data-ttu-id="83722-116">Значение</span><span class="sxs-lookup"><span data-stu-id="83722-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83722-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83722-117">Minimum supported client</span></span><br/> | <span data-ttu-id="83722-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="83722-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="83722-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83722-119">Minimum supported server</span></span><br/> | <span data-ttu-id="83722-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="83722-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="83722-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="83722-121">Redistributable</span></span><br/>          | <span data-ttu-id="83722-122">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="83722-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="83722-123">Header</span><span class="sxs-lookup"><span data-stu-id="83722-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="83722-124"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="83722-124"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="83722-125">IDL</span><span class="sxs-lookup"><span data-stu-id="83722-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="83722-126"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="83722-126"><dt>Softkbd.idl</dt></span></span> </dl> |



 

 





