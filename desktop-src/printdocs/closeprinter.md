---
description: Функция Клосепринтер закрывает указанный объект принтера.
ms.assetid: 95cc3eca-e65c-4fa6-8975-479e8e728dca
title: Функция Клосепринтер (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClosePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: ea85726220f94baeee02298246caffc70de4e688984ccd6fac3a4ac87ae11d52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720124"
---
# <a name="closeprinter-function"></a>Функция Клосепринтер

Функция **клосепринтер** закрывает указанный объект принтера.

## <a name="syntax"></a>Синтаксис


```C++
BOOL ClosePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпринтер* \[ окне\]
</dt> <dd>

Описатель для закрытого объекта принтера. Этот маркер возвращается функцией [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена, возвращаемое значение будет ненулевым.

Если функция выполняется неудачно, возвращается нулевое значение.

## <a name="remarks"></a>Remarks

> [!Note]  
> Это блокирующая или синхронная функция, которая может не возвращать значение немедленно. Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения. Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.

 

Когда функция **клосепринтер** возвращает, *хпринтер* handle является недопустимым независимо от того, была ли функция успешной или неудачной.

## <a name="examples"></a>Примеры

Пример программы, использующей эту функцию, см. в разделе [инструкции. печать с помощью API печати GDI](how-to--print-using-the-gdi-print-api.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>винспул. h (включает Windows. h)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Винспул. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>См. также

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Функции API очереди печати принтера](printing-and-print-spooler-functions.md)
</dt> <dt>

[**аддпринтер**](addprinter.md)
</dt> <dt>

[**опенпринтер**](openprinter.md)
</dt> </dl>

 

 




