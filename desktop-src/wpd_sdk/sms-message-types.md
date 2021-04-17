---
description: '\_Тип ПЕРЕЧИСЛЕНИЯ SMS Message Types \_ описывает тип содержимого сообщения SMS.'
ms.assetid: 882886a6-ecce-443f-a7e9-2e4e367ad804
title: Перечисление SMS_MESSAGE_TYPES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS_MESSAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a2e1ccfd074ff1f5287af22c5a8ebb3c6b3c661d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717862"
---
# <a name="sms_message_types-enumeration"></a><span data-ttu-id="87786-103">\_ \_ Перечисление типов сообщений SMS</span><span class="sxs-lookup"><span data-stu-id="87786-103">SMS\_MESSAGE\_TYPES enumeration</span></span>

<span data-ttu-id="87786-104">Тип **перечисления \_ SMS \_ Message** Types описывает тип содержимого сообщения SMS.</span><span class="sxs-lookup"><span data-stu-id="87786-104">The **SMS\_MESSAGE\_TYPES** enumeration type describes the content type of a short message service (SMS) message.</span></span>

## <a name="syntax"></a><span data-ttu-id="87786-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87786-105">Syntax</span></span>


```C++
typedef enum SMS_MESSAGE_TYPES { 
  SMS_TEXT_MESSAGE    = 0,
  SMS_BINARY_MESSAGE  = 1
} ;
```



## <a name="constants"></a><span data-ttu-id="87786-106">Константы</span><span class="sxs-lookup"><span data-stu-id="87786-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="87786-107"><span id="SMS_TEXT_MESSAGE"></span><span id="sms_text_message"></span>**SMS \_ Text \_ Message**</span><span class="sxs-lookup"><span data-stu-id="87786-107"><span id="SMS_TEXT_MESSAGE"></span><span id="sms_text_message"></span>**SMS\_TEXT\_MESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="87786-108">Текстовое сообщение.</span><span class="sxs-lookup"><span data-stu-id="87786-108">A text message.</span></span>

</dd> <dt>

<span data-ttu-id="87786-109"><span id="SMS_BINARY_MESSAGE"></span><span id="sms_binary_message"></span>**\_двоичное \_ сообщение SMS**</span><span class="sxs-lookup"><span data-stu-id="87786-109"><span id="SMS_BINARY_MESSAGE"></span><span id="sms_binary_message"></span>**SMS\_BINARY\_MESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="87786-110">Двоичное сообщение.</span><span class="sxs-lookup"><span data-stu-id="87786-110">A binary message.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87786-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87786-111">Remarks</span></span>

<span data-ttu-id="87786-112">Это перечисление используется [**командой "WPD" \_ \_ SMS \_ Send**](wpd-command-sms-send-command.md).</span><span class="sxs-lookup"><span data-stu-id="87786-112">This enumeration is used by the [**WPD\_COMMAND\_SMS\_SEND Command**](wpd-command-sms-send-command.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="87786-113">Требования</span><span class="sxs-lookup"><span data-stu-id="87786-113">Requirements</span></span>



| <span data-ttu-id="87786-114">Требование</span><span class="sxs-lookup"><span data-stu-id="87786-114">Requirement</span></span> | <span data-ttu-id="87786-115">Значение</span><span class="sxs-lookup"><span data-stu-id="87786-115">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="87786-116">Header</span><span class="sxs-lookup"><span data-stu-id="87786-116">Header</span></span><br/> | <dl> <span data-ttu-id="87786-117"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="87786-117"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87786-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87786-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87786-119">**Структуры и типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="87786-119">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




