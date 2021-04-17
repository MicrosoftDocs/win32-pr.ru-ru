---
title: ИВМПДВД, свойство домена
description: Свойство Domain получает текущий домен DVD-диска.
ms.assetid: 0b7b39fe-2b04-44e2-aa5e-cab7be9a06b1
keywords:
- Проигрыватель Windows Media, свойство домена
- свойство домена проигрыватель Windows Media Player, интерфейс ИВМПДВД
- Интерфейс ИВМПДВД Windows Media Player, свойство Domain
topic_type:
- apiref
api_name:
- IWMPDVD.domain
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6546a8288160fe80f7df4a7c41ea79a0edc905f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652183"
---
# <a name="iwmpdvddomain-property"></a>ИВМПДВД: свойство омаин:d

Свойство **domain** получает текущий домен DVD-диска.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String domain {get; set;}
```


```VB

Public ReadOnly Property domain As System.String
```





## <a name="property-value"></a>Значение свойства

**Строка System. String** , которая является одним из следующих значений.



| Значение                                                                                        | Значение                                                                                                                                          |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>фирстплай</dt> </dl>         | Выполнение инициализации DVD-диска по умолчанию.<br/>                                                                                      |
| <dl> <dt>видеоманажермену</dt> </dl>  | Отображение меню для всего диска. Также известен как Топмену для проигрывателя Windows Media. Обычно называется меню заголовка или верхним меню.<br/> |
| <dl> <dt>видеотитлесетмену</dt> </dl> | Отображение меню для текущего набора заголовков. Также известен как Титлемену для проигрывателя Windows Media. Обычно называется корневым меню.<br/>          |
| <dl> <dt>title</dt> </dl>             | Обычно отображение текущего заголовка.<br/>                                                                                                |
| <dl> <dt>stop</dt> </dl>              | Навигатор DVD находится в области DVD-диска.<br/>                                                                                          |
| <dl> <dt>определено</dt> </dl>         | Проигрыватель Windows Media не находится ни в одном DVD-домене.<br/>                                                                                        |



 

## <a name="remarks"></a>Комментарии

Каждый DVD-диск создан по-другому. Некоторые DVD-диски не содержат домены Фирстплай, Видеоманажермену или Видеотитлесетмену.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс ИВМПДВД (VB и C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





