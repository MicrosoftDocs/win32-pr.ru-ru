---
title: IWMPControls3 Куррентпоситионтимекоде, свойство
description: Свойство Куррентпоситионтимекоде Возвращает или задает текущую позицию в текущем элементе мультимедиа, используя формат кода времени. Сейчас это свойство поддерживает код времени SMPTE.
ms.assetid: 035b812c-e976-4b4e-b4e5-820653257732
keywords:
- проигрыватель Windows Media свойства куррентпоситионтимекоде
- проигрыватель Windows Media свойства куррентпоситионтимекоде, интерфейс IWMPControls3
- проигрыватель Windows Media интерфейса IWMPControls3, свойство куррентпоситионтимекоде
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
ms.openlocfilehash: b91c00c166050f4f3a3bc05861fa92d4fb66efcfa139e726c7cc799e21623fa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760924"
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

## <a name="remarks"></a>Remarks

Код времени SMPTE предоставляет стандартный способ идентификации отдельного кадра видео, который полезен для синхронизации воспроизведения. если файл цифрового мультимедиа поддерживает код времени SMPTE, проигрыватель Windows Media может получить сведения о текущем положении кода времени или найти кадр видео, определенный кодом времени.

Код времени SMPTE определяет конкретный кадр по количеству часов, минут, секунд и кадров, разделяющих его от определенного кадра ссылок кадром, обозначенным как нулевое время. Как правило, начальным кадром времени является начало файла, а определенное значение кода времени SMPTE представляет время, прошедшее с начала файла.

Код времени находится в формате \[  \] *чч*:*мм*:*СС*.*FF* , где \[ *Range* \] представляет диапазон, чч представляет часы, *mm* — минуты, *SS* — секунды, а *FF* — кадры. При задании значения для **куррентпоситионтимекоде** необходимо включить все восемь цифр, используя нули в качестве заполнителей.

\[*диапазон значений* \] соответствует члену **вранже** Windows в структуре **\_ \_ \_ данных расширения** Media Format вмт. дополнительные сведения о диапазонах кодов времени см. в разделе пакет SDK для Windows Media Format.

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





## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс IWMPControls3 (VB и C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





