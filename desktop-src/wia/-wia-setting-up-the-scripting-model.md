---
description: Чтобы использовать модель сценариев для получения образа Windows (WIA), необходимо, чтобы файл Wiascr.dll установлен и зарегистрирован на компьютере.
ms.assetid: 94b08833-9fbd-46cf-b6a3-71713cc6ac30
title: Настройка среды разработки модели сценариев
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6b70d52e937e93f26f95926c5ec2319611b2e8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263126"
---
# <a name="setting-up-the-scripting-model-development-environment"></a>Настройка среды разработки модели сценариев

Чтобы использовать модель сценариев для получения образа Windows (WIA), необходимо, чтобы файл Wiascr.dll установлен и зарегистрирован на компьютере.

> [!Note]  
> Эта система сценариев была заменена на уровень автоматизации службы "получение образа Windows" (WIA). См. раздел [уровень службы "получение образа Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)".

 

Скопируйте этот файл из пакета SDK для WIA в каталог *% WINDIR%*/system32 (например, c: \\ Windows \\ System32). В командной строке перейдите в этот каталог и введите **regsvr32 Wiascr.dll**.

Это приводит к вводу необходимых сведений в системный реестр.

Теперь вы готовы использовать модель скриптов WIA.

 

 
