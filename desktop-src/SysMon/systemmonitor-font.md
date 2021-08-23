---
title: Системмонитор. Font, свойство
description: Возвращает или задает шрифт, используемый в элементе управления.
ms.assetid: 973ac31e-33e6-4280-ba0b-5b9f5f7563e7
keywords:
- Свойство Font Сисмон
- Свойство Font Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, свойство Font
topic_type:
- apiref
api_name:
- SystemMonitor.Font
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a605420418c03fae69926dac5dc184f67142cad83918ab2e34dca11ea411aac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882420"
---
# <a name="systemmonitorfont-property"></a>Системмонитор. Font, свойство

Возвращает или задает шрифт, используемый в элементе управления.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
Property Font As stdole.IFontDisp
```



## <a name="property-value"></a>Значение свойства

Шрифт, используемый для вывода текста в элементе управления.

## <a name="remarks"></a>Remarks

Это внешнее свойство. Значение этого свойства определяется контейнером. Установка значения этого свойства может повлиять на иллюзию элемента управления и контейнера на одно приложение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**системмонитор**](systemmonitor.md)
</dt> <dt>

[**Системмонитор. ForeColor**](systemmonitor-forecolor.md)
</dt> </dl>

 

 





