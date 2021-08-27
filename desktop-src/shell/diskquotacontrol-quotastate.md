---
description: Задает или возвращает состояние дисковых квот тома.
title: Дисккуотаконтрол. Куотастате, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaState
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b0766ecf-6e22-4481-a6a7-df873a277bc2
ms.openlocfilehash: cb2117237cd3072163447ee80895cbbb8bb854d7ad4424da83854b28ffa96196
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090634"
---
# <a name="diskquotacontrolquotastate-property"></a>Дисккуотаконтрол. Куотастате, свойство

Задает или возвращает состояние дисковых квот тома.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```JScript
iQuotaState = DiskQuotaControl.QuotaState
DiskQuotaControl.QuotaState = iQuotaState
```



## <a name="property-value"></a>Значение свойства

Этому свойству можно присвоить одно из следующих значений.



| Состояние          | Значение | Описание               |
|----------------|-------|---------------------------|
| дкстатедисабле | 0     | Квоты диска отключены. |
| дкстатетракк   | 1     | Квоты диска отключены. |
| дкстатинфорце | 2     | Применить ограничение квоты.      |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Дисккуотаконтрол**](diskquotacontrol-object.md)
</dt> </dl>

 

 




