---
title: Основы структурированного хранилища
description: Структурированное хранилище предоставляет эквивалент полной файловой системы для хранения объектов.
ms.assetid: 7e2d6211-2ea0-4cad-9388-c789b12446ab
keywords:
- Структурированное хранилище Стрктд STG, основы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d93b74afd620edca5b6beaa43bde6fff43d7263
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890768"
---
# <a name="structured-storage-fundamentals"></a>Основы структурированного хранилища

Структурированное хранилище предоставляет эквивалент полной файловой системы для хранения объектов с помощью элементов, перечисленных в следующей таблице.



| Элемент                                                                  | Описание                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Структурированные интерфейсы хранения](structured-storage-interfaces.md)       | Интерфейсы [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)и [**ирутстораже**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) вместе с набором связанных интерфейсов —[**иперсистстораже**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)и [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream). |
| [Функции API структурированного хранилища](structured-storage-api-functions.md) | Вспомогательные API, которые упрощают реализацию структурированного хранилища, а также второй набор интерфейсов API для составных файлов; Это COM-реализация структурированных интерфейсов хранения. COM также предоставляет набор вспомогательных структур и значений перечисления, используемых для упорядочения параметров методов интерфейса и интерфейсов API.                              |
| [Структурированные режимы доступа к хранилищу](structured-storage-access-modes.md)   | Набор режимов доступа для регулирования доступа к составным файлам.                                                                                                                                                                                                                                                                                                 |



 

 

 