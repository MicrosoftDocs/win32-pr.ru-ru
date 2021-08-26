---
title: инпроксервер
description: Указывает путь к DLL внутрипроцессного сервера.
ms.assetid: f14cc8f7-e93e-4db8-8b0d-ea77a6301f33
keywords:
- COM раздела реестра Инпроксервер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b6cd1c7ab32733687292f01ddb48167c68243c62345fb17af3b6533a5cb454d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029894"
---
# <a name="inprocserver"></a>инпроксервер

Указывает путь к DLL внутрипроцессного сервера.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer
         (Default) = path
```

## <a name="remarks"></a>Remarks

Запись **инпроксервер** сравнительно редко используется для вставляемых классов.

Внутрипроцессный сервер в настоящее время зарегистрирован с помощью записи реестра **инпроксервер** . 32-разрядные и 64-битные внутрипроцессный серверы должны использовать запись [**InprocServer32**](inprocserver32.md) . Если контейнер выполняет поиск в реестре внутрипроцессного сервера, 16-разрядная версия имеет приоритет с 16-разрядным контейнером, а 32-разрядная версия имеет приоритет с 32-битным контейнером.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**InprocServer32**](inprocserver32.md)
</dt> </dl>

 

 




