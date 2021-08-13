---
title: Перекодировать содержимое с помощью интеллектуального повторного сжатия
description: Перекодировать содержимое с помощью интеллектуального повторного сжатия
ms.assetid: 02398462-b0a4-4a17-84e3-4c6f9f26639f
keywords:
- Windows Пакет SDK для формата мультимедиа, перекодирование содержимого
- Windows Пакет SDK для формата мультимедиа, интеллектуальное повторное сжатие
- Windows Пакет SDK для формата мультимедиа, повторное сжатие
- Windows пакет SDK для формата мультимедиа, Windows кодеков media Audio
- Расширенный системный формат (ASF), перекодирование содержимого
- ASF (Расширенный системный формат), перекодирование содержимого
- Расширенный системный формат (ASF), интеллектуальное повторное сжатие
- ASF (Расширенный системный формат), интеллектуальное повторное сжатие
- Расширенный формат систем (ASF), повторное сжатие
- ASF (Расширенный системный формат), повторное сжатие
- расширенный формат систем (ASF), Windows аудиокодеков мультимедиа
- ASF (расширенный системный формат), Windowsные аудиокодеки мультимедиа
- Перекодирование содержимого
- интеллектуальное повторное сжатие
- повторное сжатие
- Windows Аудиокодеки мультимедиа, перекодирование содержимого
- кодеки, Windows мультимедийные кодеки мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee1cf363e196feca81ef9757f006b211758c2ff7fbdd1f50b5136992b394f8dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699095"
---
# <a name="to-transcode-content-with-smart-recompression"></a>Перекодировать содержимое с помощью интеллектуального повторного сжатия

вы можете перекодировать содержимое из одной битовой скорости в другую с помощью пакета SDK для Windows Media Format. Как правило, это подразумевает простое декодирование содержимого и его повторное кодирование до нужной скорости. кодек Windows Media Audio 9 поддерживает интеллектуальное повторное сжатие, которое позволяет перекодировать, что достигает лучшего качества по сравнению с нормальным.

для интеллектуального повторного сжатия исходный аудиопоток должен быть закодирован с помощью аудиокодека Windows Media audio. поддерживаются все версии кодеков, но специализированные аудиокодеки (Windows media audio 9 Professional и Windows голосом media audio 9) не являются. если исходное аудио было закодировано с помощью кодека Windows Media audio 9 без потерь, нет необходимости использовать интеллектуальное повторное сжатие, так как в исходной кодировке данные не были потеряны.

Чтобы использовать интеллектуальное повторное сжатие, выполните следующие действия.

1.  Настройте объект Reader с помощью исходного файла для чтения. Дополнительные сведения см. в разделе [чтение файлов ASF](reading-asf-files.md).
2.  Настройте объект модуля записи, который будет использоваться для перекодирования файла. Задайте имя файла для нового файла. Выберите профиль, который будет использоваться для нового файла. Задайте выбранный профиль в объекте модуля записи. Дополнительные сведения см. в разделе [запись файлов ASF](writing-asf-files.md).
3.  Получите указатель на интерфейс [**ивмпрофиле**](iwmprofile.md) объекта Reader, вызвав **Ивмреадер:: QueryInterface**.
4.  Извлеките интерфейс [**ивмстреамконфиг**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) для потока аудиопотока, который необходимо перекодировать, вызвав [**Ивмпрофиле:: Stream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).
5.  Получите интерфейс [**ивммедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) для объекта конфигурации потока, вызвав **Ивмстреамконфиг:: QueryInterface**.
6.  Получите структуру [**\_ \_ типа мультимедиа WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) для потока, выполнив два вызова [**ивммедиапропс:: жетмедиатипе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Получение размера структуры при первом вызове и выделение памяти для буфера, передаваемого во второй вызов.
7.  Получите указатель на интерфейс [**ивминпутмедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) для входных данных в средстве записи, вызвав [**Ивмвритер:: жетинпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).
8.  Получите интерфейс [**ивмпропертиваулт**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) для входного объекта свойств носителя, вызвав **Ивминпутмедиапропс:: QueryInterface**.
9.  Чтобы задать свойство g всзоригиналвавеформат, используйте метод [**ивмпропертиваулт:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) \_ . Используйте структуру **вавеформатекс** , полученную на шаге 6, в качестве значения свойства.
10. Включите изменения, внесенные в свойства входного носителя, вызвав [**ивмвритер:: сетинпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) и передав ему указатель на интерфейс **ивминпутмедиапропс** .
11. Начните считывать образцы из исходного файла и передавайте их в модуль записи с помощью вызовов [**ивмвритер:: вритесампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Дополнительные разделы**](advanced-topics.md)
</dt> <dt>

[**Интерфейс Ивминпутмедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)
</dt> <dt>

[**Интерфейс Ивммедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**Интерфейс Ивмпрофиле**](iwmprofile.md)
</dt> <dt>

[**Интерфейс Ивмпропертиваулт**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)
</dt> <dt>

[**Интерфейс Ивмстреамконфиг**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> </dl>

 

 




