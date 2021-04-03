---
title: Характеристики производительности
description: Вызов реализации составного файла COM интерфейса IPropertySetStorage для создания набора свойств вызывает создание потока или хранилища с помощью вызова IStorage Креатестреам или IStorage Креатестораже.
ms.assetid: 7773e649-19a4-4df2-84ed-027d73283140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8597862602a367ed93a3d6e5e0bcac76035c337a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987660"
---
# <a name="performance-characteristics"></a>Характеристики производительности

Вызов реализации составного файла COM интерфейса [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) для создания набора свойств вызывает создание потока или хранилища с помощью вызова [**IStorage:: креатестреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) или [**IStorage:: креатестораже**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage). Набор свойств по умолчанию создается в памяти, но не сбрасывается на диск. При вызове [**ипропертистораже:: вритемултипле**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)он работает в буфере.

При открытии набора свойств используется [IStorage:: опенстреам](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) или [IStorage:: опенстораже](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) . Весь поток набора свойств считывается в смежную память. Операции [**ипропертистораже:: реадмултипле**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) работают, считывая буфер памяти. Таким образом, первый доступ требует много времени (из-за операций чтения с диска), но последующие обращения очень эффективны. Операции записи могут быть немного более ресурсоемкими, так как для обеспечения доступности дискового пространства при добавлении данных может потребоваться выполнение операций в базовом потоке.

Нет никаких гарантий относительно того, будут ли [**ипропертистораже:: вритемултипле**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) записывать обновления. Как правило, клиент должен предположить, что **ипропертистораже:: вритемултипле** обновляет только буфер в памяти. Чтобы записать данные на диск, необходимо вызвать [**ипропертистораже:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) или [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) (последний выпуск).

Такая схема означает, что [**вритемултипле**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) может быть выполнена, но данные на самом деле не сохраняются.

> [!Note]  
> Этот размер потока набора свойств не может превышать 256 КБ байт.

 

 

 