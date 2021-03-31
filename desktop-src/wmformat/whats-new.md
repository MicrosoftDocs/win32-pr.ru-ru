---
title: Новые возможности (пакет SDK для Windows Media Format 11)
description: What's New
ms.assetid: af04b99a-4653-4c82-944a-7005cf1181fe
keywords:
- Windows Media Format SDK, новые возможности
- Windows Media Format SDK, функции
- Windows Media Format SDK, новые функции
- Пакет SDK для Windows Media Format, расширенные API клиента
- Пакет Windows Media Format SDK, обновления DRM
- Пакет Windows Media Format SDK, обновления кодеков
- Windows Media Format SDK, эскизы изображений
- Управление цифровыми правами (DRM), новые функции
- DRM (Управление цифровыми правами), новые возможности
- эскизы рисунков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63d85f00f89f940ab22754d1f6f458430868d7c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800778"
---
# <a name="whats-new-windows-media-format-11-sdk"></a>Новые возможности (пакет SDK для Windows Media Format 11)

В пакете SDK для формата Windows Media 11 появились новые функции управления цифровыми правами (DRM). С момента выпуска 9,5 в пакет SDK были внесены следующие изменения.

## <a name="windows-media-drm-client-extended-apis"></a>Расширенные API клиента DRM Windows Media

Пакет SDK для Windows Media Format 11 поставляется с новым набором интерфейсов API DRM. Эти API реализованы в собственной библиотеке. Многие функции DRM, поддерживаемые объектами пакета SDK Windows Media Format, также поддерживаются расширенными API клиента DRM Windows Media. Основное различие в новых интерфейсах API заключается в том, что они не полагаются на наличие ASF-файла для работы. Вместо этого новые интерфейсы API напрямую работают с локальным хранилищем лицензий, часто используя идентификатор ключа для идентификации лицензий.

Дополнительные сведения см. в документации по [расширенным API-интерфейсам клиента DRM Windows Media](windows-media-drm-client-extended-apis.md) .

## <a name="updated-codecs"></a>Обновленные кодеки

Кодек расширенного профиля Windows Media Video 9 был обновлен для создания сжатого потока, который соответствует опубликованному стандарту VC-1 SMPTE.

В этот выпуск пакета SDK также включен кодек Windows Media Audio 10 Professional. Новый аудиокодек имеет улучшенное качество с более низкими скоростью.

## <a name="thumbnail-right"></a>Эскиз справа

Приложения могут запрашивать новое действие DRM для чтения из видео для создания эскиза изображения. Это позволяет приложениям создавать и отображать миниатюрные изображения для видеофайлов, не открывая файл для воспроизведения.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**О пакете SDK для формата Windows Media**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




