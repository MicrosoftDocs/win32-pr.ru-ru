---
description: Загружает список строк из реестра в список недавно использовавшихся (MRU).
title: 'Метод Иаклкустоммру:: Initialize'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.Initialize
api_type:
- COM
api_location: ''
ms.assetid: 358921b0-46c4-4428-b0b5-57a44fc3247b
ms.openlocfilehash: 0e0cad5f144a4ce97c648463cfdf31bf1c2ee7da0fb89b5508ce9386dba0f14f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111764"
---
# <a name="iaclcustommruinitialize-method"></a>Метод Иаклкустоммру:: Initialize

Загружает список строк из реестра в список недавно использовавшихся (MRU).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвсзмрурегкэй* \[ окне\]
</dt> <dd>

Тип: **лпквстр**

Указатель на буфер, содержащий раздел реестра со строками для списка MRU.

</dd> <dt>

*двмакс* \[ окне\]
</dt> <dd>

Тип: **DWORD**

Максимальное число записей, которые могут быть взяты из *пвсзмрурегкэй*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/> |



 

 




