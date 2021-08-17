---
description: В этом разделе приводятся общие сведения о потоковой модели с прямым управлением, способах обработки оконных сообщений путем непосредственной обработки и о том, как состояние окна просмотра изменяется в качестве входных данных, сопоставленных с выходными движениями.
ms.assetid: 0818E34E-990E-4C36-9954-EF87EB226AF6
title: Обработка входных данных с помощью Директманипулатион
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 49b72f88da8978192af402c8b810655c102395d5aad273f34340ed57e2703008
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094662"
---
# <a name="processing-input-with-directmanipulation"></a>Обработка входных данных с помощью Директманипулатион

В этом разделе приводятся общие сведения о потоковой модели с [прямым](direct-manipulation-portal.md) управлением, способах обработки оконных сообщений путем непосредственной обработки и о том, как состояние окна просмотра изменяется в качестве входных данных, сопоставленных с выходными движениями.

- [Поток ввода](#input-flow)
- [Замечания](#remarks)

При [непосредственной манипуляции](direct-manipulation-portal.md) для координации асинхронных операций используются два потока:

*Поток пользовательского интерфейса* — это поток, которому принадлежит **HWND** , связанный с входными данными. Этот поток владеет принадлежащей инициализации [непосредственной манипуляции](direct-manipulation-portal.md). Обработка ввода с помощью мыши и клавиатуры также происходит в потоке пользовательского интерфейса.

*Поток делегата* — это поток, созданный и принадлежащий [непосредственной манипуляции](direct-manipulation-portal.md). Обработка входных данных сенсорного ввода происходит в потоке делегата.

## <a name="input-flow"></a>Поток ввода

В типичной конфигурации, в которой проверка попадания выполняется в потоке пользовательского интерфейса, сообщения окон обрабатываются путем [непосредственной манипуляции](direct-manipulation-portal.md) в следующем порядке:

![Схема, показывающая порядок обработки сообщений.](images/inputprocessing.png)

Для окна просмотра неактивных:

1. Ряд оконных сообщений достигает потока делегата.
2. [WM_POINTERDOWN](../inputmsg/wm-pointerdown.md) и [DM_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) сообщения отправляются потоком делегата в поток независимого теста попаданий (ИХТ).
3. Если [**сетконтакт**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) вызывается из потока ИХТ, сообщения могут отправляться в поток пользовательского интерфейса потоком делегата, в зависимости от значения [**директманипулатион \_ HITTEST \_ Type**](/windows/win32/api/directmanipulation/ne-directmanipulation-directmanipulation_hittest_type) при вызове [**регистерхиттесттаржет**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget) .
4. Если [**сетконтакт**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) не вызывается из потока ИХТ, то сообщения всегда отправляются потоком делегата в поток пользовательского интерфейса.
5. Клиент может вызвать [**сетконтакт**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) из потока пользовательского интерфейса, чтобы позволить [прямой манипуляции](direct-manipulation-portal.md) обнаруживать манипуляцию.
6. При обнаружении манипуляции [Непосредственная манипуляция](direct-manipulation-portal.md) отправляет сообщение [WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md) для уведомления клиента о том, что входные данные обрабатываются посредством непосредственной манипуляции. Для окна просмотра задано состояние **выполняется** и преобразование выходных данных будет обновлено.
7. Если обнаруживается взаимодействие, не связанное с манипуляцией, [Непосредственная манипуляция](direct-manipulation-portal.md) отправляет оставшиеся сообщения в поток пользовательского интерфейса.

Для окна просмотра в движении (с состоянием "выполняется" или "ИНЕРЦИя") сообщение окна достигает потока делегата, где тесты нажатия [прямых манипуляций](direct-manipulation-portal.md) выполняются для всех работающих окон просмотра. При непосредственной манипуляции контакт автоматически назначается соответствующим окнам просмотра, определенным при проверке нажатия. Состояние окна просмотра — "выполняется", а преобразование "выход" будет обновлено.

В некоторых случаях поток пользовательского интерфейса приложения может оказаться слишком медленным для реагирования на проверку попадания. Можно использовать поток проверки нажатия ([**регистерхиттесттаржет**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget)), чтобы позволить клиенту перемещать сообщения [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) и [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) в конкретный поток, чтобы разрешить проверку попадания.

## <a name="remarks"></a>Remarks

Как правило, [Непосредственная манипуляция](direct-manipulation-portal.md) отправляет сообщения [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) и [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) в поток пользовательского интерфейса, задерживая последующие сообщения при ожидании ответа от клиента. Если клиент вызывает [**сетконтакт**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact), то только сообщения, получаемые ПОТОКОМ пользовательского интерфейса при обнаружении манипуляции, — это [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) и [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md), а также [сообщение WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md).

Клиент может не вызывать [**сетконтакт**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) при обработке сообщений [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) и [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) . В этом случае [Непосредственная манипуляция](direct-manipulation-portal.md) отправляет все сообщения в поток пользовательского интерфейса без анализа сообщений, чтобы проверить, существует ли манипуляция. Затем клиент может выбрать любую точку для вызова **сетконтакт** , чтобы начать обнаружение манипуляций и отправить сообщения [WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md) при обнаружении одного.

**Windows 10 и более поздних версий:** Вы можете решить, какие манипуляции необходимо обрабатывать, вызвав [**деферконтакт**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationdefercontactservice-defercontact) перед вызовом [**Сетконтакт**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) в сообщении [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) или [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) . **Деферконтакт** гарантирует, что все последующие сообщения отправляются в поток пользовательского интерфейса в течение указанного периода времени.
