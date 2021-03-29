---
description: Отображение диалоговых окон записи VFW
ms.assetid: 708212ca-d148-4079-8052-3bf6696a33ab
title: Отображение диалоговых окон записи VFW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b8b51b164630a8fa6e91b2e68ca8a9a3a875b6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805387"
---
# <a name="display-vfw-capture-dialog-boxes"></a>Отображение диалоговых окон записи VFW

Устройство записи, которое по-прежнему использует драйвер Video для Windows (VFW), может поддерживать любое из следующих трех диалоговых окон, которые используются для настройки устройства.



| .    | Описание                                                                                           |
|---------------|-------------------------------------------------------------------------------------------------------|
| Источник видео  | Используется для выбора входных данных видео и для настройки параметров устройства, таких как яркость или контрастность изображения. |
| Формат видео  | Используется для выбора размеров изображения и битовой глубины.                                                    |
| Отображение видео | Используется для управления внешним видом отображаемого видео.                                                 |



 

Чтобы отобразить одно из этих диалоговых окон, выполните следующие действия.

1.  Останавливает граф фильтра.
2.  Запросите фильтр записи для интерфейса [**иамвфвкаптуредиалогс**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) . Если **QueryInterface** проходит успешнее, это означает, что устройство записи является устройством VFW.
3.  Вызовите метод [**иамвфвкаптуредиалогс:: хасдиалог**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) , чтобы проверить, поддерживает ли драйвер диалоговое окно, которое необходимо отобразить. Перечисление [**вфвкаптуредиалогс**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) определяет флаги для каждого из диалоговых окон VFW. **Хасдиалог** возвращает значение \_ ОК, если диалоговое окно поддерживается. \_В противном случае возвращается значение false, поэтому следует проверить наличие значения \_ ОК напрямую, а не использовать макрос **успешно** .
4.  Если диалоговое окно поддерживается, вызовите метод [**иамвфвкаптуредиалогс:: ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) , чтобы отобразить диалоговое окно.
5.  Перезапустите граф.

В следующем коде показаны эти шаги для диалогового окна источник видео.


```C++
pControl->Stop(); // Stop the graph.

// Query the capture filter for the IAMVfwCaptureDialogs interface.
IAMVfwCaptureDialogs *pVfw = 0;
hr = pCap->QueryInterface(IID_IAMVfwCaptureDialogs, (void**)&pVfw);
if (SUCCEEDED(hr))
{
    // Check if the device supports this dialog box.
    if (S_OK == pVfw->HasDialog(VfwCaptureDialog_Source))
    {
        // Show the dialog box.
        hr = pVfw->ShowDialog(VfwCaptureDialog_Source, hwndParent);
    }
}
pControl->Run();
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Настройка устройства видеозаписи](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



