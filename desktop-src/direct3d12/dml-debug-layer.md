---
title: Использование слоя отладки Директмл
description: Уровень отладки Директмл — это дополнительный компонент времени разработки, который помогает в отладке кода Директмл.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: f885595e5cc3b3890d208875fb92e47e0dc5e337
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "104548973"
---
# <a name="using-the-directml-debug-layer"></a>Использование слоя отладки Директмл

Уровень отладки Директмл — это дополнительный компонент времени разработки, который помогает в отладке кода Директмл. Слой отладки является частью отдельного пакета графических средств, распространяемого как [функция по требованию](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (FOD). Для использования слоя отладки в системе должны быть установлены средства Graphics Tools FOD.

Мы настоятельно рекомендуем включить уровень отладки при разработке приложений с помощью Директмл, так как он может предоставить ценную информацию в случае недопустимого использования API.

## <a name="installing-the-directml-debug-layer"></a>Установка слоя отладки Директмл

Чтобы установить дополнительный пакет по запросу для графических инструментов (FOD), выполните следующую команду в командной строке администратора PowerShell.

```powershell
Add-WindowsCapability -Online -Name "Tools.Graphics.DirectX~~~~0.0.1.0"
```

Кроме того, пакет средств для обработки графики можно установить с помощью параметров Windows 10. Перейдите к разделу **Параметры**  >  **приложения приложения**  >  **& функции**  >  **Дополнительные функции**  >  **Добавить компонент** > затем выберите **графические инструменты**.

## <a name="enabling-the-directml-debug-layer"></a>Включение слоя отладки Директмл

После установки пакета средств для обработки графики можно включить уровень отладки Директмл, указав  [**DML_CREATE_DEVICE_FLAG_DEBUG**](/windows/win32/api/directml/ne-directml-dml_create_device_flags) при вызове [**дмлкреатедевице**](/windows/win32/api/directml/nf-directml-dmlcreatedevice).

> [!IMPORTANT]
> Сначала необходимо включить уровень отладки Direct3D 12. А *затем* включите уровень отладки директмл, вызвав **дмлкреатедевице**.

После включения слоя отладки Директмл все ошибки Директмл или недопустимые вызовы API приведут к выдаче отладочной информации в качестве выходных данных отладки. Пример приведен ниже.

```console
DML_OPERATOR_CONVOLUTION: invalid D3D12_HEAP_TYPE. DirectML requires all bound buffers to be D3D12_HEAP_TYPE_DEFAULT.
```

## <a name="see-also"></a>См. также раздел

* [Функция Дмлкреатедевице](/windows/win32/api/directml/nf-directml-dmlcreatedevice)
* [Доступные функции — по запросу](/windows-hardware/manufacture/desktop/features-on-demand-non-language-fod)
* [Использование проверки на основе GPU с уровнем отладки Direct3D 12](/windows/desktop/direct3d12/using-d3d12-debug-layer-gpu-based-validation)
* [Справочник по отладочному слою Direct3D 12](/windows/desktop/direct3d12/direct3d-12-sdklayers-reference)
