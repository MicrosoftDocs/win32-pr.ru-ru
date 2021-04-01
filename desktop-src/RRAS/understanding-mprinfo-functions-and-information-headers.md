---
title: Основные сведения о функциях и заголовках Мпринфо
description: Для следующих функций необходимо, чтобы вызывающий объект передал информационную структуру или заголовок в качестве одного из параметров.
ms.assetid: 389002c9-2d24-4b35-ab5b-801fe2091db9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 001c39bf28500d7261b3eb99abf0266470daf3d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986539"
---
# <a name="understanding-mprinfo-functions-and-information-headers"></a>Основные сведения о функциях и заголовках Мпринфо

Для следующих функций необходимо, чтобы вызывающий объект передал информационную структуру или *заголовок* в качестве одного из параметров.



| Функция администрирования                                                        | Функция настройки                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| Нет функции администрирования                                                     | [**мпрконфигтранспорткреате**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportcreate)                     |
| [**мпрадминтранспортсетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo)                   | [**мпрконфигтранспортсетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo)                   |
| [**мпрадмининтерфацетранспортсетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) | [**мпрконфигинтерфацетранспортсетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) |
| [**мпрадмининтерфацетранспортадд**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportadd)         | [**мпрконфигинтерфацетранспортадд**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportadd)         |



 

Аналогичным образом следующие функции возвращают заголовки данных.



| Функция администрирования                                                        | Функция настройки                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**мпрадминтранспортжетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo)                   | [**мпрконфигтранспортжетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo)                   |
| [**мпрадмининтерфацетранспортжетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) | [**мпрконфигинтерфацетранспортжетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) |



 

Для транспортных функций заголовок Information содержит глобальные сведения для транспорта. Для функций клиента (Интерфацетранспорт) в заголовке содержатся сведения, относящиеся к администрированием клиента (например, OSPF).

Заголовки данных и их содержимое следует манипулировать только с помощью функций [мпринфо](router-information-functions.md) . Разработчикам не следует пытаться управлять содержимым заголовков данных напрямую.

В таких функциях, как [**мпрадмининтерфацесетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) , не требуется использовать функции мпринфо. Сведения, которые передаются и возвращаются с помощью этих функций, всегда находятся в виде [**структуры \_ интерфейса MPR**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) .

 

 




