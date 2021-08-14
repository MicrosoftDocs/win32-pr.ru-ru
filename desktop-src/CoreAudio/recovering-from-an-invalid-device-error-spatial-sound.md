---
description: Восстановление после ошибки Invalid-Device (пространственный звук)
title: Восстановление после ошибки Invalid-Device (пространственный звук)
ms.topic: article
ms.date: 10/29/2020
ms.openlocfilehash: 124d4a804c2f99c051fee50d1c8d819d794b87a5943c216951e0c72870de8c18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406222"
---
# <a name="recovering-from-an-invalid-device-error-spatial-sound"></a>Восстановление после ошибки Invalid-Device (пространственный звук)

Многие методы API-интерфейса пространственного звука (Майкрософт), такие как [испатиалаудиоклиент](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), [испатиалаудиубжектрендерстреам](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)и [испатиалаудиубжект](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), возвращают коды ошибок, если устройство конечной точки аудио, используемое клиентским приложением, становится недопустимым или в конечной точке изменился формат пространственного звука. Эти коды ошибок указывают на то, что устройство конечной точки было отключено или перенастроено, отключено, удалено, режим пространственного звука или же недоступно для использования. Часто приложение может восстановиться после этой ошибки.

Коды ошибок, указывающие на ошибку недопустимого устройства, включают следующее:

- SPTLAUDCLNT_E_DESTROYED
- AUDCLNT_E_DEVICE_INVALIDATED
- AUDCLNT_E_RESOURCES_INVALIDATED
- AUDCLNT_E_UNSUPPORTED_FORMAT
- SPTLAUDCLNT_E_INTERNAL

## <a name="strategies-for-handling-invalid-device-errors"></a>Стратегии обработки недопустимых ошибок устройства

Рекомендуемая стратегия восстановления после ошибки недопустимого устройства зависит от того, будет ли приложение автоматически выбирать определенное устройство в соответствии с внутренними требованиями или пользователь может явно выбрать устройство из списка доступных устройств. 

### <a name="default-audio-device"></a>Звуковое устройство по умолчанию

Если приложение автоматически выбирает устройство по умолчанию, выполните следующие действия для восстановления.

1. Освободите интерфейс [испатиалаудиубжектрендерстреам](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) и [испатиалаудиоклиент](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) и любые другие пространственные аудио интерфейсы, используемые для отрисовки. 
1. Вызовите [иммдевицеенумератор:: жетдефаултаудиоендпоинт](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) , чтобы получить текущее звуковое устройство по умолчанию.
1. Попытка активировать **испатиалаудиоклиент** на звуковом устройстве.
1. Активация **испатиалаудиубжектрендерстреам**. 

### <a name="specifically-selected-audio-device"></a>Конкретное выбранное звуковое устройство

Если приложение выбирает определенное звуковое устройство, выполните следующие действия для восстановления.

1. Освободите интерфейс Испатиалаудиубжектрендерстреам и любые другие пространственные аудио интерфейсы, которые используются для отрисовки, но не выпускайте **испатиалаудиоклиент**.
1. Используйте текущий экземпляр **испатиалаудиоклиент** для активации **испатиалаудиубжектрендерстреам**.

Обратите внимание, что для обеих стратегий, перечисленных выше, одни и те же действия можно применить к приложениям, использующим интерфейсы [испатиалаудиубжектрендерстреамформетадата](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) или [испатиалаудиубжектрендерстреамфорхртф](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) . Просто замените **испатиалаудиубжектрендерстреам** в описанных выше шагах на интерфейсы Metadata или хртф.


## <a name="related-topics"></a>Связанные темы

<dl> <dt>
[Восстановление после ошибки Invalid-Device](recovering-from-an-invalid-device-error.md) 
 [Управление потоками](stream-management.md)
</dt> </dl>

 

 



