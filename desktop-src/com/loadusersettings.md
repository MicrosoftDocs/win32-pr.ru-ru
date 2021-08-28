---
title: лоадусерсеттингс
description: Определяет, будет ли COM загружать профиль пользователя для COM-серверов, запущенных в качестве запускающего удостоверения пользовательского приложения.
ms.assetid: 3e2b3249-3747-4d98-96da-f3e480a51d12
keywords:
- COM-значение реестра Лоадусерсеттингс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b82bd89015baa4c73c9200013e49c76523951218dfde62bbe39300eefdfe0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731044"
---
# <a name="loadusersettings"></a>лоадусерсеттингс

Определяет, будет ли COM загружать профиль пользователя для COM-серверов, запущенных в качестве запускающего удостоверения пользовательского приложения.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LoadUserSettings = value
```

## <a name="remarks"></a>Remarks

Это значение **reg \_ DWORD** . Если *значение* не равно нулю, com загружает профиль учетной записи пользователя, с помощью которой он запускает COM-сервер. Если *значение* равно нулю или отсутствует, com не будет загружать профиль учетной записи пользователя, с помощью которой он запускает COM-сервер.

Этот параметр игнорируется, если имеется запись [**запуска от имени**](runas.md) .

 

 




