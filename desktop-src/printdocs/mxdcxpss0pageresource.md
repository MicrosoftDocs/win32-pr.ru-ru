---
description: Структура МКСДК \_ XPS \_ S0PAGE \_ Resource \_ T содержит сведения о ресурсе, например изображение или шрифт, который связан со страницей документа XPS и передается в выходной файл конвертера документов Microsoft XPS (мксдк).
ms.assetid: af0690a6-3047-4e95-b719-2305948c0f5d
title: Структура MXDC_XPS_S0PAGE_RESOURCE_T (Мксдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_XPS_S0PAGE_RESOURCE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 21035a99b6237c481a5b7560f469086ef2960d655ba32582ed273edb48910ba8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971183"
---
# <a name="mxdc_xps_s0page_resource_t-structure"></a>\_Структура мксдк XPS \_ S0PAGE \_ Resource \_ T

Структура **мксдк \_ XPS \_ S0PAGE \_ Resource \_ T** содержит сведения о ресурсе, например изображение или шрифт, который связан со страницей документа XPS и передается в выходной файл конвертера документов Microsoft XPS (мксдк).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMxdcXpsS0PageResource {
  DWORD dwSize;
  DWORD dwResourceType;
  BYTE  szUri[MAX_PATH];
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_XPS_S0PAGE_RESOURCE_T, *P_MXDC_XPS_S0PAGE_RESOURCE_T;
```



## <a name="members"></a>Члены

<dl> <dt>

**двсизе**
</dt> <dd>

Общий размер этой структуры и ресурса, на который она указывает.

</dd> <dt>

**двресаурцетипе**
</dt> <dd>

Значение типа [**мксдк \_ S0 \_ \_ перечисление страниц**](mxdcs0pageenums.md) , указывающее тип ресурса, например изображение TIFF или шрифт TrueType.

</dd> <dt>

**сзури**
</dt> <dd>

Универсальный код ресурса (URI) для данного ресурса. Это не может быть более 260 байт.

</dd> <dt>

**двдатасизе**
</dt> <dd>

Размер ресурса в байтах.

</dd> <dt>

**бдата**
</dt> <dd>

Данные ресурса в массиве байтов с размером 1 + Размер ресурса.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура добавляется в структуру [**мксдк \_ Escape- \_ заголовка \_ T**](mxdcescapeheader.md) (для которой в качестве **кода операции** задано значение **мксдкоп \_ Set \_ S0PAGERESOURCE**), чтобы сделать [**мксдк \_ S0PAGE \_ ресурса \_ \_ t**](mxdcs0pageresourceescape.md) -структурой. Полученная **Структура \_ \_ Escape- \_ последовательности \_ ресурсов мксдк S0PAGE** передается в параметр *лпсзиндата* функции [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) , которая вызывается с помощью escape- [**последовательности \_ мксдк**](mxdc-escape.md) . Результатом является отправка ресурса в МКСДК для преобразования и его запись в выходной файл.

Вызов [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) должен быть между вызовом [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) и вызовом [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); Однако между вызовами **StartPage** и **EndPage** может быть несколько таких вызовов.

Потоковая передача данных более эффективна, если вы вызываете [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) с **кодом операции** **\_ \_ S0PAGE \_ ресурса мксдкоп Set** для каждого ресурса на странице перед вызовом **екстескапе** с **мксдкоп \_ Set \_ S0PAGE** **.**

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                    |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                              |
| Заголовок<br/>                   | <dl> <dt>Мксдк. h</dt> </dl> |



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

 

