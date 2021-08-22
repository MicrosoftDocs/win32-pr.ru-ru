---
description: Используется для управления состоянием яркости датчика внешнего освещения.
ms.assetid: ff400d4e-be8c-450b-ad53-d43b0ab84ab3
title: Метод Вмисеталсбригхтнессстате класса Вмимониторбригхтнессмесодс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightnessState
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 1c8a99ea92391626975d635802f82dd81b663247f4bb3522db19d14237d920f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051122"
---
# <a name="wmisetalsbrightnessstate-method-of-the-wmimonitorbrightnessmethods-class"></a>Метод Вмисеталсбригхтнессстате класса Вмимониторбригхтнессмесодс

Метод **вмисеталсбригхтнессстате** используется для управления состоянием яркости датчика внешнего освещения. Если при использовании метода [**вмисетбригхтнесс**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) было установлено переопределение яркости, то это переопределение будет иметь приоритет над заданной для Кроме яркости, используя этот метод. Чтобы переопределение КРОМЕной яркости вступило в силу, необходимо отменить политику яркости, используя метод [**вмиреверттополицибригхтнесс**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) .

## <a name="syntax"></a>Синтаксис


```mof
uint32 WmiSetALSBrightnessState(
   boolean State
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Состояние* 
</dt> <dd>

Состояние яркости Кроме. Значение false отключает переопределение яркости Кроме, а значение true включает его.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ноль (0), чтобы указать на успешное выполнение. Любое другое значение указывает на ошибку. Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Пространство имен<br/>                | Корневой \\ инструментарий WMI<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Вмикоре. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**вмимониторбригхтнессмесодс**](wmimonitorbrightnessmethods.md)
</dt> <dt>

[**мсмониторкласс**](msmonitorclass.md)
</dt> </dl>

 

