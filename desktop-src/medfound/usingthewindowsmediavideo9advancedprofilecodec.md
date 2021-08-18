---
description: использование расширенного профиля Windows Media Video 9
ms.assetid: 2abc0efc-dd11-4921-897c-209a26f8ba1d
title: использование расширенного профиля Windows Media Video 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 258c32f14d1a7a42e1450c8265e2a611bd17b3b92b98f5433c93b91251e299c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012174"
---
# <a name="using-the-windows-media-video-9-advanced-profile"></a>использование расширенного профиля Windows Media Video 9

базовые видеопроцедуры, описанные в разделе [работа с видео](workingwithvideo.md) , также применяются непосредственно к расширенному профилю Windows Media video 9. Никаких специальных процедур не требуется.

расширенный профиль Windows Media Video 9 связан с идентификаторами классов clsid \_ CWMV9EncMediaObject и clsid \_ квмвдекмедиаобжект. Значение FOURCC для типов мультимедиа, использующих этот кодек, — "WVC1".

расширенный профиль Windows Media Video 9 поддерживает все общие режимы кодирования, а также чередующиеся кодировки, смешанные, чередующиеся и прогрессивные кодировки, разрешения, отличные от отображаемых, и функции уменьшения диапазона. Другая возможность — возможность хранить метаданные последовательности и кадра в самом побитовом потоке; ранее это требовало использования интерфейса ASF и API модулей обработки данных.

следующие свойства расширенного профиля Windows Media Video 9, которые можно контролировать с помощью параметров реестра, не имеют соответствующих строк **ипропертибаг** или **ипропертисторе** :

-   Параметр дкуант.
-   Сила дкуант.
-   Принудительно перекрытие.
-   Метод стоимости вектора движения.

## <a name="achieving-optimal-visual-quality"></a>Достижение оптимального визуального качества

для большинства видеоданных, чтобы обеспечить оптимальное качество визуального элемента с помощью расширенного профиля Windows Media video 9, можно присвоить свойству [ \_ компрессионоптимизатионтипе мфпкэй](mfpkey-compressionoptimizationtypeproperty.md) значение 1.

## <a name="about-the-previous-windows-media-video-9-advanced-profile-codecs"></a>о предыдущих Windows кодеках расширенного профиля Media видео 9

текущая версия микрокодека расширенного профиля Windows Media Video 9 базируется на обществах для расширенного профиля VC-1 (SMPTE 421M) (SMPTE) standard. этот кодек заменяет более раннюю кодек с Windows также называется кодеком Windows Media Video 9 Advanced Profile, который был идентифицирован с помощью кода FOURCC "вмва". Предыдущая версия кодека VC-1 была реализована до завершения предыдущего стандарта расширенного профиля VC-1 и больше не поддерживается.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Работа с видео](workingwithvideo.md)
</dt> 
<dt>

[использование расширенного Параметры кодека Windows Media видео 9 advanced Profile](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)
</dt> </dl>

 

 



