---
title: Класс Win32_WinSAT
description: Определяет сведения о сводных оценках для последней формальной оценки.
ms.assetid: adf4de42-9dfd-46a7-ae75-3bbcfd15dd68
keywords:
- Win32_WinSAT класс WinSAT
- Win32_WinSAT класс WinSAT, описание
topic_type:
- apiref
api_name:
- Win32_WinSAT
- Win32_WinSAT.TimeTaken
- Win32_WinSAT.WinSPRLevel
- Win32_WinSAT.WinSATAssessmentState
- Win32_WinSAT.MemoryScore
- Win32_WinSAT.CPUScore
- Win32_WinSAT.DiskScore
- Win32_WinSAT.D3DScore
- Win32_WinSAT.GraphicsScore
api_location:
- WinSATAPI.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829e5e1b3658771728aab9ef30634d90a8bc6450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701093"
---
# <a name="win32_winsat-class"></a>\_Класс Win32 WinSAT

\[**Win32 \_ Служба WinSAT** может быть изменена или недоступна для выпусков после Windows 8.1.\]

Определяет сведения о сводных оценках для последней формальной оценки.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
class Win32_WinSAT
{
  string TimeTaken = "MostRecentAssessment";
  real32 WinSPRLevel;
  uint32 WinSATAssessmentState;
  real32 MemoryScore;
  real32 CPUScore;
  real32 DiskScore;
  real32 D3DScore;
  real32 GraphicsScore;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ WinSAT** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ WinSAT** имеет следующие свойства.

<dl> <dt>

**кпускоре**
</dt> <dd> <dl> <dt>

Тип данных: **real32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Оценка процессоров на компьютере.

</dd> <dt>

**D3DScore**
</dt> <dd> <dl> <dt>

Тип данных: **real32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

После Windows 8.1 WinSAT больше не оценивает трехмерные графические (игровые) возможности компьютера, а также возможность графического драйвера для отрисовки объектов и выполнения шейдеров с помощью этой оценки. Для обеспечения совместимости значения Sentinel отчета WinSAT для метрик и оценок не рассчитываются в режиме реального времени.

</dd> <dt>

**дискскоре**
</dt> <dd> <dl> <dt>

Тип данных: **real32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Оценка пропускной способности последовательного чтения на основном жестком диске компьютера.

</dd> <dt>

**графиксскоре**
</dt> <dd> <dl> <dt>

Тип данных: **real32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Оценка графических возможностей компьютера.

</dd> <dt>

**меморискоре**
</dt> <dd> <dl> <dt>

Тип данных: **real32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Оценка пропускной способности и емкости компьютера в памяти.

</dd> <dt>

**TimeTaken**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Это свойство должно иметь значение "Мострецентассессмент" в предложении WHERE WQL-запроса.

</dd> <dt>

**винсатассессментстате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Состояние оценки. Описание возможных значений см. в разделе Перечисление [**\_ \_ состояния оценки WinSAT**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state) .

<dl> <dt>

<span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**Статеункновн** (0)
</dt> <dt>

<span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**Допустимый** (1)
</dt> <dt>

<span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**Инкохерентвисхардваре** (2)
</dt> <dt>

<span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**Ноассессментаваилабле** (3)
</dt> <dt>

<span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Недопустимое** (4)
</dt> </dl>

</dd> <dt>

**винспрлевел**
</dt> <dd> <dl> <dt>

Тип данных: **real32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Базовый показатель для компьютера. Дополнительные сведения о значении оценки см. в описании свойства [**ипровидевинсатресултсинфо:: системратинг**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Сведения о оценках подкомпонентов, например **меморискоре**, см. в описании свойства [**Ипровидевинсатассессментинфо:: Score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) .

## <a name="examples"></a>Примеры

Пример, демонстрирующий использование инструментария WMI для получения данных из этого класса, см. в описании метода [**ипровидевинсатвисуалс:: Get \_ Bitmap**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WinSAT. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>WinSATAPI.dll</dt> </dl> |



 

 





