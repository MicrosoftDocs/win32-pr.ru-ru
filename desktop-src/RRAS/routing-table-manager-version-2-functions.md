---
title: Функции диспетчера таблиц маршрутизации версии 2
description: Для взаимодействия с диспетчером таблиц маршрутизации используются следующие функции.
ms.assetid: ac5c6ada-c38e-476a-9896-cdd8c51cc0be
keywords:
- Служба маршрутизации и удаленного доступа RRAS, диспетчер таблиц маршрутизации, версия 2, функции
- Диспетчер таблиц маршрутизации, службы RRAS версии 2, функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb7138b54ee0fa747c7d367c54d7a0fb893c3d2d451577932c669650a0fc76e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026924"
---
# <a name="routing-table-manager-version-2-functions"></a>Функции диспетчера таблиц маршрутизации версии 2

Для взаимодействия с диспетчером таблиц маршрутизации используются следующие функции.

## <a name="registration-functions"></a>Функции регистрации

[**ртмрегистерентити**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity)

[**ртмдерегистерентити**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity)

[**ртмжетрегистередентитиес**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities)

[**ртмрелеасинтитиес**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities)

## <a name="opaque-pointer-functions"></a>Функции непрозрачных указателей

[**ртмлоккдестинатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination)

[**ртмжетопакуеинформатионпоинтер**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer)

## <a name="export-method-functions"></a>Функции метода Export

[**ртмжетентитимесодс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods)

[**ртминвокемесод**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod)

[**ртмблоккмесодс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods)

## <a name="handle-to-information-structure-functions"></a>Обработчик для функций структуры информации

[**ртмжетентитинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo)

[**ртмжетдестинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo)

[**ртмжетраутеинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)

[**ртмжетнекссопинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo)

[**ртмрелеасинтитинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo)

[**ртмрелеаседестинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo)

[**ртмрелеасераутеинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo)

[**ртмрелеасенекссопинфо**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)

## <a name="routing-table-insertion-and-deletion-functions"></a>Функции вставки и удаления таблиц маршрутизации

[**ртмаддраутетодест**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest)

[**ртмделетераутетодест**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutetodest)

[**ртмхолддестинатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination)

[**ртмжетраутепоинтер**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetroutepointer)

[**ртмлоккрауте**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute)

[**ртмупдатеандунлоккрауте**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute)

## <a name="routing-table-query-functions"></a>Функции запроса таблицы маршрутизации

[**ртмжетексактматчдестинатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination)

[**ртмжетмостспеЦификдестинатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination)

[**ртмжетлессспеЦификдестинатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination)

[**ртмжетексактматчрауте**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute)

[**ртмисбестрауте**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute)

## <a name="next-hop-insertion-and-deletion-functions"></a>Функции вставки и удаления следующего прыжка

[**ртмадднекссоп**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop)

[**ртмфинднекссоп**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop)

[**ртмделетенекссоп**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop)

[**ртмжетнекссоппоинтер**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthoppointer)

[**ртмлоккнекссоп**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop)

## <a name="routing-table-enumeration-functions"></a>Функции перечисления таблиц маршрутизации

[**ртмкреатедестенум**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum)

[**ртмжетенумдестс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests)

[**ртмрелеаседестс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests)

[**ртмкреатераутинум**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum)

[**ртмжетенумраутес**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes)

[**ртмрелеасераутес**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes)

[**ртмкреатенекссопенум**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum)

[**ртмжетенумнекссопс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops)

[**ртмрелеасенекссопс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops)

[**ртмделетинумхандле**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle)

## <a name="change-notification-functions"></a>Функции уведомлений об изменениях

[**ртмрегистерфорчанженотификатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification)

[**ртмжетчанжеддестс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests)

[**ртмрелеасечанжеддестс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasechangeddests)

[**ртмигноречанжеддестс**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests)

[**ртмжетчанжестатус**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus)

[**ртммаркдестфорчанженотификатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification)

[**ртмисмаркедфорчанженотификатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmismarkedforchangenotification)

[**ртмдерегистерфромчанженотификатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification)

## <a name="route-list-function"></a>Функция списка маршрутов

[**ртмкреатераутелист**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelist)

[**ртминсертинраутелист**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminsertinroutelist)

[**ртмкреатераутелистенум**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelistenum)

[**ртмжетлистенумраутес**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlistenumroutes)

[**ртмделетераутелист**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutelist)

## <a name="handle-management-functions"></a>Функции управления обработчиками

[**ртмреференцехандлес**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles)

 

 




