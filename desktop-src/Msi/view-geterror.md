---
description: Метод GetObject объекта View возвращает ошибку проверки и имя столбца, для которого произошла ошибка.
ms.assetid: ca90dfa5-8e15-490c-835b-c5c225c3cc7b
title: Метод View. с ошибками
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.GetError
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ddbed26565598ad58b3605b7c70a9a5bbede3e5282ff4a7fa011df5c56bd8b31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038804"
---
# <a name="viewgeterror-method"></a>Метод View. с ошибками

Метод GetObject объекта [**View**](view-object.md) **возвращает ошибку проверки** и имя столбца, для которого произошла ошибка. В службе автоматизации возвращаемое значение является строкой вида \# \# ColumnName, где — \# \# 2-значный код ошибки. Он возвращает первую ошибку в массиве ошибок представления. последующие вызовы возвращают следующее значение в массиве ошибок. После возвращения значения "00" больше ошибок не существует, и последующие вызовы просто проводят через массив снова.

## <a name="syntax"></a>Синтаксис


```JScript
View.GetError()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView определен как 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




