---
description: '\_ \_ \_ Escape-структура ресурса мксдк S0PAGE \_ представляет собой структуру t мксдк ~, \_ \_ \_ объединенную с \_ структурой мксдк XPS \_ S0PAGE \_ Resource \_ t.'
ms.assetid: e5caa280-f0a5-4a89-b4f1-4f195a537dc6
title: Структура MXDC_S0PAGE_RESOURCE_ESCAPE_T (Мксдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_RESOURCE_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: ed1d78aad1ede2a318dcde2d3a2d39fd8e666ddc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264449"
---
# <a name="mxdc_s0page_resource_escape_t-structure"></a>\_ \_ Структура переключения ресурсов мксдк S0PAGE \_ \_ T

Escape-структура **\_ \_ ресурса \_ мксдк \_ S0PAGE** представляет собой структуру [**\_ \_ \_ t мксдк**](mxdcescapeheader.md) ~, объединенную с структурой [**мксдк \_ XPS \_ S0PAGE \_ Resource \_ t**](mxdcxpss0pageresource.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMxdcS0PageResourceEscape {
  MXDC_ESCAPE_HEADER_T       mxdcEscape;
  MXDC_XPS_S0PAGE_RESOURCE_T xpsS0PageResourcePassthrough;
} MXDC_S0PAGE_RESOURCE_ESCAPE_T, *P_MXDC_S0PAGE_RESOURCE_ESCAPE_T;
```



## <a name="members"></a>Члены

<dl> <dt>

**мксдцескапе**
</dt> <dd>

Структура [**мксдк \_ Escape- \_ заголовка \_ T**](mxdcescapeheader.md) с набором элементов **opcode** , равным мксдкоп \_ Set \_ S0PAGE \_ Resource.

</dd> <dt>

**xpsS0PageResourcePassthrough**
</dt> <dd>

Структура [**мксдк \_ XPS \_ S0PAGE \_ Resource \_ T**](mxdcxpss0pageresource.md) , представляющая ресурс, например шрифт или файл изображения, на странице документа XPS.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта структура передается в параметре *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) , когда эта функция вызывается с помощью escape-экранирования [**Мксдк \_**](mxdc-escape.md) , а элемент **кода операции** в структуре [**мксдк \_ Escape- \_ заголовка \_ T**](mxdcescapeheader.md) — **мксдкоп \_ Set \_ S0PAGE \_ Resource**. Результатом является ресурс страницы для отправки в МКСДК.

Выделите память для экранирования, как показано ниже, задайте необходимые поля, а затем вызовите [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_RESOURCE_ESCAPE_T) + 
                        iS0PageResourceDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_RESOURCE_ESCAPE_T pS0PageResourceEscapeData = 
                        (P_MXDC_S0PAGE_RESOURCE_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



Вызов [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) должен быть между вызовом [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) и вызовом [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); Однако между вызовами **StartPage** и **EndPage** может быть больше одного из этих вызовов.

Потоковая передача данных более эффективна, если вы вызываете [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) с **кодом операции** **\_ \_ S0PAGE \_ ресурса мксдкоп Set** для каждого ресурса на странице перед вызовом **екстескапе** с **мксдкоп \_ Set \_ S0PAGE****.**  

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                    |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                              |
| Header<br/>                   | <dl> <dt>Мксдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> <dt>

[Escape-функции принтера GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**Escape-МКСДК \_**](mxdc-escape.md)
</dt> </dl>

 

