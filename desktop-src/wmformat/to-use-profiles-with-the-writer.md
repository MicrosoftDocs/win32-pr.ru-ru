---
title: Использование профилей с модулем записи
description: Использование профилей с модулем записи
ms.assetid: 8805bc57-5f19-4544-bcb8-5af880ba8ea0
keywords:
- Windows Пакет SDK для формата мультимедиа, написание файлов ASF
- Windows Пакет SDK для формата мультимедиа, создание файлов ASF
- Windows Пакет SDK формата мультимедиа, расширенный формат систем (ASF)
- Расширенный системный формат (ASF), запись файлов
- ASF (Расширенный системный формат), запись файлов
- Расширенный системный формат (ASF), создание файлов
- ASF (Расширенный системный формат), создание файлов
- профили, создание файлов ASF
- профили, запись файлов ASF
- профили, создание файлов ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0184469215dd109bcc4ca120e2db9cbead8b9bd250cb017456f9d7d08ea46f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027272"
---
# <a name="to-use-profiles-with-the-writer"></a>Использование профилей с модулем записи

Модуль записи использует данные профиля для создания файлов ASF. Необходимо указать профиль для использования перед выполнением каких-либо других действий с модулем записи.

Вы можете задать системный профиль для модуля записи, передав идентификатор профиля в метод [**ивмвритер:: сетпрофилебид**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) .

Чтобы указать настраиваемый профиль для использования с модулем записи, необходимо получить интерфейс [**ивмпрофиле**](iwmprofile.md) для объекта, содержащего данные требуемого профиля. Для этого можно использовать один из методов загрузки интерфейса [**ивмпрофилеманажер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) . После создания допустимого интерфейса **ивмпрофиле** можно передать указатель на него в метод [**Ивмвритер:: сетпрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) . Дополнительные сведения о параметрах профиля см. [в разделе Работа с профилями](working-with-profiles.md).

При внесении изменений в объект Profile с помощью интерфейса **ивмпрофиле** после задания профиля в средстве записи необходимо вызвать **сетпрофиле** повторно, иначе изменения не будут отражены в модуле записи. Однако вызов **сетпрофиле** приведет к сбросу всех атрибутов заголовка, поэтому обязательно задайте необходимые атрибуты заголовка после вызова этого метода.

следующий пример функции задает для профиля значение "Windows Media Video 8 для коммутируемых модемов (56 кбит/с)":


```C++
#include <wmsysprf.h>

HRESULT SetProfileExample()
{
  HRESULT hr;
  IWMWriter *pWriter = NULL;
  hr = WMCreateWriter(NULL, &pWriter);
  if (FAILED(hr)) return hr;
  hr = pWriter->SetProfileByID(WMProfile_V80_56Video);
  return hr;
}

```



> [!Note]  
> нет стандартных системных профилей, использующих кодеки Windows Media Audio и Video 9. Дополнительные сведения см. в разделе [повторное использование конфигураций потоков](reusing-stream-configurations.md).

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Ивмвритер:: Сетпрофилебид**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)
</dt> <dt>

[**Работа с профилями**](working-with-profiles.md)
</dt> <dt>

[**Запись файлов ASF**](writing-asf-files.md)
</dt> </dl>

 

 




