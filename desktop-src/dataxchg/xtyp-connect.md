---
title: XTYP_CONNECTная транзакция (Ддемл. h)
description: Клиент использует \_ транзакцию кстип Connect для создания диалога.
ms.assetid: 74f43b10-f7ac-4370-9caa-7b9ddf3413ed
keywords:
- XTYP_CONNECT обмена данными транзакций
topic_type:
- apiref
api_name:
- XTYP_CONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2268994f1be000373691d6c25dbb7220d3e109e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136163"
---
# <a name="xtyp_connect-transaction"></a>\_Транзакция кстип Connect

Клиент использует транзакцию **кстип \_ Connect** для создания диалога. Функция обратного вызова сервера платформа динамических данных Exchange (DDE) получает эту транзакцию [*, когда*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)клиент указывает имя службы, которое поддерживает сервер (и имя раздела, не равное **null**) в вызове функции [**ддеконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) .


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_CONNECT            (0x0060 | XCLASS_BOOL | XTYPF_NOBLOCK)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*утипе* 
</dt> <dd>

Тип транзакции.

</dd> <dt>

*уфмт* 
</dt> <dd>

Не используется.

</dd> <dt>

*хконв* 
</dt> <dd>

Не используется.

</dd> <dt>

*hsz1* 
</dt> <dd>

Маркер имени раздела.

</dd> <dt>

*hsz2* 
</dt> <dd>

Описатель имени службы.

</dd> <dt>

*хдата* 
</dt> <dd>

Не используется.

</dd> <dt>

*dwData1* 
</dt> <dd>

Указатель на структуру [**конвконтекст**](/windows/win32/api/ddeml/ns-ddeml-convcontext) , содержащую сведения о контексте для диалога. Если клиент не является приложением ДДЕМЛ, этот параметр равен 0.

</dd> <dt>

*dwData2* 
</dt> <dd>

Указывает, является ли клиент тем же экземпляром приложения, что и сервер. Если параметр равен 1, то клиент является тем же экземпляром. Если параметр равен 0, то клиент является другим экземпляром.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция обратного вызова сервера должна возвращать **значение true** , чтобы позволить клиенту устанавливать диалог с заданной парой имени службы и имени раздела, или функция должна возвращать **значение false** , чтобы запретить диалог. Если функция обратного вызова возвращает **значение true** и диалог успешно установлен, система передает этот обработчик на сервер, выполняя транзакцию [**кстип \_ Connect \_ Confirm**](xtyp-connect-confirm.md) для функции обратного вызова сервера (если только сервер не указал флаг **КБФ \_ Skip \_ Connect \_** в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) ).

## <a name="remarks"></a>Комментарии

Эта транзакция фильтруется, если серверное приложение указало флаг **КБФ \_ Failed \_ Connections** в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Сервер не может заблокировать этот тип транзакции; код **возврата \_ блока CBR** игнорируется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                   |
| Заголовок<br/>                   | <dl> <dt>Ддемл. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**конвконтекст**](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[**ддеконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Зрения**
</dt> <dt>

[Библиотека управления платформа динамических данных Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

