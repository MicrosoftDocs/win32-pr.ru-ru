---
title: Функции контекста взаимодействия
description: В подразделах этого раздела приведены справочные спецификации для функций контекста взаимодействия.
ms.assetid: 0F34F181-D92C-4B08-9F1D-62379D4A2B15
keywords:
- взаимодействие с пользователем
- input
- указатель
- Сенсорный ввод
- Мышь
- Перо
- перо
ms.topic: article
ms.date: 02/06/2020
ms.openlocfilehash: 5f0769aa5b9b097b23206c0515bd32552a59969404e72bbfcf26973d5d4f3de6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758340"
---
# <a name="interaction-context-functions"></a>Функции контекста взаимодействия

В подразделах этого раздела приведены справочные спецификации для функций [контекста взаимодействия](interaction-context-portal.md) .

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|---|---|
| [**аддпоинтеринтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-addpointerinteractioncontext)<br/> | Включить указанный указатель в набор указателей, обрабатываемых объектом [контекста взаимодействия](interaction-context-portal.md) . <br/> |
| [**буфферпоинтерпаккетсинтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-bufferpointerpacketsinteractioncontext)<br/> | Добавляет журнал для одного входного указателя в буфер объекта [контекста взаимодействия](interaction-context-portal.md) .<br/> |
| [**креатеинтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-createinteractioncontext)<br/> | Создает и инициализирует объект [контекста взаимодействия](interaction-context-portal.md) .<br/> |
| [**дестройинтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-destroyinteractioncontext)<br/> | Уничтожает указанный объект [контекста взаимодействия](interaction-context-portal.md) .<br/> |
| [**жеткроссслидепараметеринтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-getcrossslideparameterinteractioncontext)<br/> | Возвращает поведение взаимодействия между слайдами. <br/> |
| [**жетинертиапараметеринтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-getinertiaparameterinteractioncontext)<br/> | Возвращает поведение инерции для манипуляции (преобразование, вращение, масштабирование). <br/> |
| [**жетинтерактионконфигуратионинтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-getinteractionconfigurationinteractioncontext)<br/> | Возвращает состояние конфигурации взаимодействия для объекта [контекста взаимодействия](interaction-context-portal.md) .<br/> |
| [**жетмаусевхилпараметеринтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-getmousewheelparameterinteractioncontext)<br/> | Возвращает состояние колесика мыши для объекта [контекста взаимодействия](interaction-context-portal.md) . <br/> |
| [**жетпропертинтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-getpropertyinteractioncontext)<br/> | Возвращает свойства объекта [контекста взаимодействия](interaction-context-portal.md) .<br/> |
| [**жетстатеинтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-getstateinteractioncontext)<br/> | Возвращает текущее состояние [контекста взаимодействия](interaction-context-portal.md) и время, когда контекст возвращается в состояние бездействия. <br/> |
| [**процессбуффередпаккетсинтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-processbufferedpacketsinteractioncontext)<br/> | Обработка буферизованных пакетов в конце входного кадра указателя.<br/> |
| [**процессинертиаинтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-processinertiainteractioncontext)<br/> | Отправляет входные данные таймера в объект [контекста взаимодействия](interaction-context-portal.md) для обработки инерции.<br/> |
| [**процесспоинтерфрамесинтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-processpointerframesinteractioncontext)<br/> | Обрабатывает набор входных кадров указателя.<br/> |
| [**регистераутпуткаллбаккинтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-registeroutputcallbackinteractioncontext)<br/> | Регистрирует обратный вызов для получения событий взаимодействия из объекта [контекста взаимодействия](interaction-context-portal.md) .<br/> |
| [**ремовепоинтеринтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-removepointerinteractioncontext)<br/> | Удаляет указанный указатель из набора указателей, обработанных объектом [контекста взаимодействия](interaction-context-portal.md) . <br/> |
| [**ресетинтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-resetinteractioncontext)<br/> | Сбрасывает [**состояние взаимодействия**](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_state), параметры конфигурации взаимодействия и все параметры в исходное состояние. Текущие взаимодействия отменяются без уведомлений. <br/> Перед следующим использованием необходимо перенастроить [контекст взаимодействия](interaction-context-portal.md) .<br/> |
| [**сеткроссслидепараметерсинтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-setcrossslideparametersinteractioncontext)<br/> | Настраивает взаимодействие между слайдами. <br/> |
| [**сетинертиапараметеринтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-setinertiaparameterinteractioncontext)<br/> | Настраивает поведение инерции (преобразование, вращение, масштабирование) после того, как связь с ним ликвидируется. <br/> | [**сетинтерактионконфигуратионинтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-setinteractionconfigurationinteractioncontext)<br/> | Настраивает объект [контекста взаимодействия](interaction-context-portal.md) для обработки указанных манипуляций.<br/> |
| [**сетмаусевхилпараметеринтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-setmousewheelparameterinteractioncontext)<br/> | Задает значения параметров для входных данных колесика мыши. <br/> |
| [**сетпивотинтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-setpivotinteractioncontext)<br/> | Задает центральную точку и радиус поворота от центральной точки для обработки вращения с помощью одного указателя ввода. <br/> |
| [**сетпропертинтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-setpropertyinteractioncontext)<br/> | Задает свойства объекта [контекста взаимодействия](interaction-context-portal.md) .<br/> |
| [**стопинтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)<br/> | Устанавливает [**состояние взаимодействия**](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_state) в \_ состояние \_ простоя взаимодействия и оставляет все параметры конфигурации взаимодействия и параметры без изменений. Текущие взаимодействия отменяются и уведомления отправляются по мере необходимости.<br/> Перенастройка [контекста взаимодействия](interaction-context-portal.md) перед следующим использованием невозможна.<br/> |

## <a name="related-topics"></a>Связанные темы

[Справочник по контексту взаимодействия](interaction-context-reference.md)
