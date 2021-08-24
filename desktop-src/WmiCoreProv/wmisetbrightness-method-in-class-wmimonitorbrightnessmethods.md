---
description: Задает яркость экрана монитора компьютера.
ms.assetid: 900cf5fd-6888-4f0b-8e0b-01eeaaeeeb8f
title: Метод Вмисетбригхтнесс класса Вмимониторбригхтнессмесодс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 0a9425668ad00422033a77233ade2822966db0f19d6e6628ada24866be9953f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794444"
---
# <a name="wmisetbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a>Метод Вмисетбригхтнесс класса Вмимониторбригхтнессмесодс

Метод **вмисетбригхтнесс** задает яркость экрана монитора компьютера.

## <a name="syntax"></a>Синтаксис


```mof
uint32 WmiSetBrightness(
   uint32 Timeout,
   uint8  Brightness
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Timeout* 
</dt> <dd>

Время ожидания в секундах.

</dd> <dt>

*Brightness* 
</dt> <dd>

Яркость в процентах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ноль (0), чтобы указать на успешное выполнение. Любое другое значение указывает на ошибку. Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

## <a name="examples"></a>Примеры

Дополнительные сведения о получении и настройке яркости монитора см. в блоге, посвященном [использованию PowerShell для создания отчетов и настройки яркости](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx) монитора.

В следующем примере PowerShell яркость монитора устанавливается равным 50%.


```PowerShell
$brightness = 50
$delay = 5
$myMonitor = Get-WmiObject -Namespace root\wmi -Class WmiMonitorBrightnessMethods
$myMonitor.wmisetbrightness($delay, $brightness)
```



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

 

