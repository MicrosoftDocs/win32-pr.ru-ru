---
description: SetPriority&\# 32; Метод класса WMI пытается изменить приоритет выполнения процесса.
ms.assetid: ef012e9e-ff65-4881-835e-ddab23af9333
ms.tgt_platform: multiple
title: Метод SetPriority класса Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.SetPriority
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: decd5892d480e4f236ae9d7acdc1a25c018557166535c963eb35dc3f6f62ffa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675573"
---
# <a name="setpriority-method-of-the-win32_process-class"></a>Метод SetPriority \_ класса процесса Win32

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) SetPriority пытается изменить приоритет выполнения процесса.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Приоритет* \[ окне\]
</dt> <dd>

Новый класс приоритета для процесса. Обратите внимание, что эти значения отличаются от значений, явно указанных в свойстве **Priority** [**\_ процесса Win32**](win32-process.md).

<dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Бездействие** (64)


</dt> <dd>

Задается для процесса с потоками, которые выполняются только при бездействии системы. Потоки процесса прерываются потоками процесса, который выполняется в классе с более высоким приоритетом, например экранной заставкой. Класс с приоритетом простоя наследуется дочерними процессами.

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Ниже среднего** (16384)


</dt> <dd>

Обозначает процесс, который имеет приоритет **над \_ \_ классом приоритета простоя**, но ниже **обычного \_ \_ класса приоритета**.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Обычная** (32)


</dt> <dd>

Задается для процесса без особых потребностей в планировании.

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Выше обычного** (32768)


</dt> <dd>

Обозначает процесс, который имеет приоритет над **нормальным \_ \_ классом приоритета**, но ниже **класса с высоким \_ приоритетом \_**.

</dd> <dt>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**Высокий приоритет** (128)


</dt> <dd>

Задается для процесса, который выполняет критические по времени задачи, которые должны выполняться немедленно. Потоки процесса выгружают потоки процессов с нормальными или низкими приоритетами. Примером может быть список задач, который должен быстро реагировать при вызове пользователем, независимо от нагрузки на операционную систему. При использовании класса с высоким приоритетом необходимо соблюдать осторожность, так как приложение класса с высоким приоритетом может использовать почти все доступное время ЦП.

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Реальное** (256)


</dt> <dd>

Задается для процесса, имеющего наивысший возможный приоритет. Потоки процесса выгружают потоки всех других процессов, включая процессы операционной системы, выполняющие важные задачи. Например, процесс в режиме реального времени, который выполняется в течение более короткого интервала, может привести к тому, что дисковые кэши не будут сбрасываться или мышь не будет отвечать на запросы.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений, перечисленных в следующем списке, или другое значение, указывающее на ошибку. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Успешное завершение** (0)
</dt> <dt>

**Отказано в доступе** (2)
</dt> <dt>

**Недостаточно прав доступа** (3)
</dt> <dt>

**Неизвестный сбой** (8)
</dt> <dt>

**Путь не найден** (9)
</dt> <dt>

**Недопустимый параметр** (21)
</dt> <dt>

**Другие** (22 4294967295)
</dt> </dl>

## <a name="remarks"></a>Remarks

чтобы установить приоритет в режиме реального времени, вызывающая сторона должна иметь права **SeIncreaseBasePriorityPrivilege** (с **\_ \_ базовым \_ приоритетом \_ SE INC**). Без этой привилегии наивысший приоритет можно задать с высоким приоритетом.

## <a name="examples"></a>Примеры

В примере [изменения приоритета выполняемого процесса](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) VBScript изменяется приоритет запущенного экземпляра Notepad.exe с обычного на выше нормального.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Процесс Win32**](win32-process.md)
</dt> </dl>

 

