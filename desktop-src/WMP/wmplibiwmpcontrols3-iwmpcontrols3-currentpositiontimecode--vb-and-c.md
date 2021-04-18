---
title: IWMPControls3 Куррентпоситионтимекоде, свойство
description: Свойство Куррентпоситионтимекоде Возвращает или задает текущую позицию в текущем элементе мультимедиа, используя формат кода времени. Сейчас это свойство поддерживает код времени SMPTE.
ms.assetid: 035b812c-e976-4b4e-b4e5-820653257732
keywords:
- Проигрыватель Windows Media для свойства Куррентпоситионтимекоде
- Куррентпоситионтимекоде свойство проигрывателя Windows Media Player, интерфейс IWMPControls3
- Интерфейс IWMPControls3 Windows Media Player, свойство Куррентпоситионтимекоде
topic_type:
- apiref
api_name:
- IWMPControls3.currentPositionTimecode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7660e6dc2690c310cf06f64e38190dc1cb3f24ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649054"
---
# <a name="iwmpcontrols3currentpositiontimecode-property"></a>Свойство IWMPControls3:: Куррентпоситионтимекоде

Свойство **куррентпоситионтимекоде** Возвращает или задает текущую позицию в текущем элементе мультимедиа, используя формат кода времени. Сейчас это свойство поддерживает код времени SMPTE.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String currentPositionTimecode {get; set;}
```


```VB

Public Property currentPositionTimecode As System.String
```





## <a name="property-value"></a>Значение свойства

**Строка System. String** , которая является кодом времени SMPTE.

## <a name="remarks"></a>Комментарии

Код времени SMPTE предоставляет стандартный способ идентификации отдельного кадра видео, который полезен для синхронизации воспроизведения. Если файл цифрового мультимедиа поддерживает код времени SMPTE, проигрыватель Windows Media может получить сведения о текущем положении кода времени или найти кадр видео, определенный кодом времени.

Код времени SMPTE определяет конкретный кадр по количеству часов, минут, секунд и кадров, разделяющих его от определенного кадра ссылок кадром, обозначенным как нулевое время. Как правило, начальным кадром времени является начало файла, а определенное значение кода времени SMPTE представляет время, прошедшее с начала файла.

Код времени находится в формате \[  \] *чч*:*мм*:*СС*.*FF* , где \[ *Range* \] представляет диапазон, чч представляет часы, *mm* — минуты, *SS* — секунды, а *FF* — кадры. При задании значения для **куррентпоситионтимекоде** необходимо включить все восемь цифр, используя нули в качестве заполнителей.

\[*диапазон значений* \] соответствует члену **вранже** структуры **\_ \_ \_ данных расширения** времени в формате Windows Media ВМТ. Дополнительные сведения о диапазонах кодов времени см. в разделе Windows Media Format SDK.

Установка и получение **куррентпоситионтимекоде** поддерживаются только для файлов, содержащих сведения о коде времени SMPTE.

## <a name="examples"></a>Примеры

В следующем примере кода указывается **куррентпоситионтимекоде** в виде 1 часа, 0 минут, 30 секунд и 5 кадров. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
// Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
// so that you can use the currentPositionTimecode property.
WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

// Seek to a frame using SMPTE time code.
controls.currentPositionTimecode = "[00000]01:00:30.05";
```


```VB

' Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
&#39; so that you can use the currentPositionTimecode property.
Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

&#39; Seek to a frame using SMPTE time code.
Controls.currentPositionTimecode = &quot;[00000]01:00:30.05&quot;
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс IWMPControls3 (VB и C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





