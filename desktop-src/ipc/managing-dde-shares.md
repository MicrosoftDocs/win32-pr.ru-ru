---
description: Сетевой DDE предоставляет функции, позволяющие удалять общую папку, получать или задавать сведения о ресурсах или перечислять общие папки.
ms.assetid: d7924e93-75e4-4f94-b159-02408535170d
title: Управление общими ресурсами DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa89b890c9cf2b140f669b5e4dfa556cd11f978d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472170"
---
# <a name="managing-dde-shares"></a>Управление общими ресурсами DDE

\[Сетевой DDE больше не поддерживается. Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают ндде \_ не \_ реализованы.\]

Сетевой DDE предоставляет функции, позволяющие удалять общую папку, получать или задавать сведения о ресурсах или перечислять общие папки.




| Задача | Процедура | 
|------|-----------|
| Удаление общего ресурса DDE | Используйте функцию <a href="nddesharedel.md"><strong>нддешаредел</strong></a> . | 
| Получение сведений об общем ресурсе DDE | Используйте функцию <a href="nddesharegetinfo.md"><strong>нддешарежетинфо</strong></a> . | 
| Задать сведения об общем ресурсе DDE | Используйте функцию <a href="nddesharesetinfo.md"><strong>нддешаресетинфо</strong></a> . | 
| Перечисление общих ресурсов DDE | Используйте функцию <a href="nddeshareenum.md"><strong>нддешаринум</strong></a> . Вы также можете перечислить доверенные общие ресурсы DDE с помощью функции <a href="nddetrustedshareenum.md"><strong>нддетрустедшаринум</strong></a> .<br /> | 
| Перечисление подключенных пользователей | Используйте функцию <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>нетсессионенум</strong></a> . | 
| Изменение имени общего ресурса DDE | Удалите старую общую папку и создайте новую.<ol><li>Получите сведения об общем ресурсе с помощью <a href="nddesharegetinfo.md"><strong>нддешарежетинфо</strong></a>.</li><li>Удалите общую папку с помощью <a href="nddesharedel.md"><strong>нддешаредел</strong></a>.</li><li>Измените элемент <strong>лпсзшаренаме</strong> структуры <a href="nddeshareinfo-str.md"><strong>нддешареинфо</strong></a> , возвращенной <a href="nddesharegetinfo.md"><strong>нддешарежетинфо</strong></a>.</li><li>Передайте измененную структуру <a href="nddeshareinfo-str.md"><strong>нддешареинфо</strong></a> в <a href="nddeshareadd.md"><strong>нддешареадд</strong></a>.</li></ol> | 




 

 

