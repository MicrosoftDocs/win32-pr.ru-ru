---
description: Приложение может программно создавать и удалять каталоги.
ms.assetid: 52d1d8a8-e5a7-44f5-9bf2-2a496ef79d32
title: Создание и удаление каталогов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140547594271e13bc78bfa78336f167f228879a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155299"
---
# <a name="creating-and-deleting-directories"></a>Создание и удаление каталогов

Приложение может программно создавать и удалять каталоги.

Чтобы создать новый каталог, используйте функцию [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya), [**креатедиректорекс**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)или [**креатедиректоритрансактед**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) . Каталогу присваивается имя, указанное при его создании. Соглашения об именовании каталога следуют правилам именования файлов. Описание этих соглашений см. [в разделе Присвоение имени файлу](naming-a-file.md).

Чтобы удалить существующий каталог, используйте функцию [**ремоведиректори**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) или [**ремоведиректоритрансактед**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) . Перед удалением каталога необходимо убедиться, что каталог пуст и у вас есть права на удаление для каталога. Чтобы выполнить Последнее действие, вызовите функцию [**жетсекуритинфо**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) .

 

 
