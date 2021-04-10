---
title: Структура ORPC_DBG_ALL
description: Структура ОРПК \_ dbg \_ ALL используется для передачи параметров методам интерфейса иорпкдебугнотифи.
ms.assetid: 05371beb-9202-40a6-96d2-4b91497e2ee9
keywords:
- ORPC_DBG_ALL структуры COM
- COM LPORPC_DBG_ALL указателя структуры
topic_type:
- apiref
api_name:
- ORPC_DBG_ALL
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17f5b09e5fe2f668bf2bcd21e2e7fe6f0f766a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135494"
---
# <a name="orpc_dbg_all-structure"></a>ОРПК \_ \_ структуру dbg ALL

Структура **ОРПК \_ dbg \_ ALL** используется для передачи параметров методам интерфейса [**иорпкдебугнотифи**](iorpcdebugnotify.md) .

> [!Note]  
> Каждый метод интерфейса [**иорпкдебугнотифи**](iorpcdebugnotify.md) использует другое сочетание членов, приведенных ниже. Если член не обозначен как используемый методом, он не определен при передаче в этот метод.

 

## <a name="syntax"></a>Синтаксис


```C++
typedef struct ORPC_DBG_ALL {
  BYTE              *pSignature;
  RPCOLEMESSAGE     *pMessage;
  const IID         *refiid;
  IRpcChannelBuffer *pChannel;
  IUnknown          *pUnkProxyMgr;
  void              *pInterface;
  IUnknown          *pUnkObject;
  HRESULT           hresult;
  void              *pvBuffer;
  ULONG             *cbBuffer;
  ULONG             *lpcbBuffer;
  void              *reserved;
} ORPC_DBG_ALL, *LPORPC_DBG_ALL;
```



## <a name="members"></a>Члены

<dl> <dt>

**псигнатуре**
</dt> <dd>

Указатель на буфер **байтов** , содержащий:

-   Первые четыре байта: символы ASCII "МАРБ" при увеличении порядка памяти.
-   Следующие 16 байт: **идентификатор GUID** , определяющий вызываемое уведомление. Он содержит один из следующих элементов:
    1.  [**Клиентжетбуфферсизе**](iorpcdebugnotify-clientgetbuffersize.md): 9ED14F80-9673-101A-B07B-00DD01113F11
    2.  [**Клиентфиллбуффер**](iorpcdebugnotify-clientfillbuffer.md):D a45f3e0-9673-101A-B07B-00DD01113F11
    3.  [**Клиентнотифи**](iorpcdebugnotify-clientnotify.md): 4F60E540-9674-101A-B07B-00DD01113F11
    4.  [**Сервернотифи**](iorpcdebugnotify-servernotify.md): 1084FA00-9674-101A-B07B-00DD01113F11
    5.  [**Сервержетбуфферсизе**](iorpcdebugnotify-servergetbuffersize.md): 22080240-9674-101A-B07B-00DD01113F11
    6.  [**Серверфиллбуффер**](iorpcdebugnotify-serverfillbuffer.md): 2FC09500-9674-101A-B07B-00DD01113F11
-   Следующие четыре байта: зарезервировано для будущего использования.

> [!Note]
>
> Используется всеми методами интерфейса [**иорпкдебугнотифи**](iorpcdebugnotify.md) .

 

</dd> <dt>

**пмессаже**
</dt> <dd>

Указатель на структуру [**рпколемессаже**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) , содержащую сведения о маршалинге данных RPC.

> [!Note]
>
> Используется методами [**клиентфиллбуффер**](iorpcdebugnotify-clientfillbuffer.md), [**клиентжетбуфферсизе**](iorpcdebugnotify-clientgetbuffersize.md), [**клиентнотифи**](iorpcdebugnotify-clientnotify.md), [**серверфиллбуффер**](iorpcdebugnotify-serverfillbuffer.md), [**сервержетбуфферсизе**](iorpcdebugnotify-servergetbuffersize.md)и [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**рефиид**
</dt> <dd>

Указатель на идентификатор IID интерфейса [**иорпкдебугнотифи**](iorpcdebugnotify.md) .

> [!Note]
>
> Используется методами [**клиентфиллбуффер**](iorpcdebugnotify-clientfillbuffer.md), [**клиентжетбуфферсизе**](iorpcdebugnotify-clientgetbuffersize.md), [**клиентнотифи**](iorpcdebugnotify-clientnotify.md), [**серверфиллбуффер**](iorpcdebugnotify-serverfillbuffer.md), [**сервержетбуфферсизе**](iorpcdebugnotify-servergetbuffersize.md)и [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**пчаннел**
</dt> <dd>

Указатель на интерфейс [**ирпкчаннелбуффер**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) реализации com-канала RPC на сервере.

> [!Note]
>
> Используется методами [**серверфиллбуффер**](iorpcdebugnotify-serverfillbuffer.md), [**сервержетбуфферсизе**](iorpcdebugnotify-servergetbuffersize.md)и [**сервернотифи**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**пункпроксимгр**
</dt> <dd>

Указатель на интерфейс [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) объекта, участвующий в этом вызове отладчика. Может иметь **значение NULL**, однако это сокращает функциональность отладчика.

> [!Note]
>
> Используется методами [**клиентфиллбуффер**](iorpcdebugnotify-clientfillbuffer.md), [**клиентжетбуфферсизе**](iorpcdebugnotify-clientgetbuffersize.md)и [**клиентнотифи**](iorpcdebugnotify-clientnotify.md) .

 

</dd> <dt>

**пинтерфаце**
</dt> <dd>

Указатель на COM-интерфейс метода, который будет вызываться этим RPC. Не может иметь **значение NULL**.

> [!Note]
>
> Используется методами [**серверфиллбуффер**](iorpcdebugnotify-serverfillbuffer.md), [**сервержетбуфферсизе**](iorpcdebugnotify-servergetbuffersize.md)и [**сервернотифи**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**Объект punkObject**
</dt> <dd>

Должен иметь **значение NULL**.

> [!Note]
>
> Используется методами [**серверфиллбуффер**](iorpcdebugnotify-serverfillbuffer.md), [**сервержетбуфферсизе**](iorpcdebugnotify-servergetbuffersize.md)и [**сервернотифи**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**состав**
</dt> <dd>

Назначение этого участника изменяется для каждого из уведомлений ниже:

[**Клиентжетбуфферсизе**](iorpcdebugnotify-clientgetbuffersize.md): число байтов, которое клиентский отладчик будет передавать в серверный отладчик. Если значение равно нулю, сведения не передаются.

[**Клиентнотифи**](iorpcdebugnotify-clientnotify.md): значение **HRESULT** последнего удаленного вызова процедуры.

[**Сервержетбуфферсизе**](iorpcdebugnotify-servergetbuffersize.md): число байтов, которое клиентский отладчик будет передавать в серверный отладчик. Если значение равно нулю, сведения не передаются.

> [!Note]
>
> Используется методами [**клиентжетбуфферсизе**](iorpcdebugnotify-clientgetbuffersize.md), [**клиентнотифи**](iorpcdebugnotify-clientnotify.md)и [**сервержетбуфферсизе**](iorpcdebugnotify-servergetbuffersize.md) .

 

</dd> <dt>

**пвбуффер**
</dt> <dd>

Указатель на структуру [**буфера ОРПК \_ dbg \_**](orpc-dbg-buffer.md) , содержащую сведения об упакованной отладке RPC. Не определен, если **кббуффер** равен нулю.

> [!Note]
>
> Используется методами [**клиентфиллбуффер**](iorpcdebugnotify-clientfillbuffer.md), [**клиентнотифи**](iorpcdebugnotify-clientnotify.md), [**серверфиллбуффер**](iorpcdebugnotify-serverfillbuffer.md)и [**сервернотифи**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**кббуффер**
</dt> <dd>

Длина (в байтах) данных, на которые указывает **пвбуффер**.

> [!Note]
>
> Используется методами [**клиентфиллбуффер**](iorpcdebugnotify-clientfillbuffer.md), [**клиентнотифи**](iorpcdebugnotify-clientnotify.md), [**серверфиллбуффер**](iorpcdebugnotify-serverfillbuffer.md)и [**сервернотифи**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**лпкббуффер**
</dt> <dd>

Число байтов, которое клиентский отладчик будет передавать в серверный отладчик. Если значение равно нулю, сведения не передаются. Это значение заменяет значение, возвращаемое в **HRESULT**.

> [!Note]
>
> Используется методами [**клиентфиллбуффер**](iorpcdebugnotify-clientfillbuffer.md), [**клиентжетбуфферсизе**](iorpcdebugnotify-clientgetbuffersize.md) .

 

</dd> <dt>

**процессу**
</dt> <dd>

Зарезервировано. Не используется.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                     |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                           |
| Заголовок<br/>                   | <dl> <dt>Н/Д</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_БУФЕР ОРПК dbg \_**](orpc-dbg-buffer.md)
</dt> <dt>

[**\_аргументы инициализации \_ ОРПК**](orpc-init-args.md)
</dt> <dt>

[**дллдебугобжектрпчук**](dlldebugobjectrpchook.md)
</dt> <dt>

[**иорпкдебугнотифи**](iorpcdebugnotify.md)
</dt> </dl>

 

