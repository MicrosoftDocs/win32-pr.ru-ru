---
description: Метод Сетассинглетон объекта Свбемобжектпас заставляет путь обращаться к единственному экземпляру WMI класса. Одноэлементный класс — это класс, который не может иметь более одного экземпляра.
ms.assetid: 7ec53954-2aac-494c-87c7-6a14592d8bd5
ms.tgt_platform: multiple
title: Свбемобжектпас. Сетассинглетон, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4a8a46566990021a4de4fca95b2b524cc7ddc1f5a797d7e3bffd0dc34ee52186
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568264"
---
# <a name="swbemobjectpathsetassingleton-method"></a>Свбемобжектпас. Сетассинглетон, метод

Метод **сетассинглетон** объекта [**свбемобжектпас**](swbemobjectpath.md) заставляет путь обращаться к единственному экземпляру WMI класса. Одноэлементный класс — это класс, который не может иметь более одного экземпляра.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md). свбемобжектпас

## <a name="syntax"></a>Синтаксис


```VB
SWbemObjectPath.SetAsSingleton()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **сетассинглетон** объект **Err** может содержать приведенный ниже код ошибки.

<dl> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМОБЖЕКТПАС CLSID<br/>                                                       |
| IID<br/>                      | IID \_ исвбемобжектпас<br/>                                                        |



 

 




