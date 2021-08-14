---
description: Извлекает перечислитель, возвращающий один указатель на список идентификаторов элементов (ПИДЛ) для каждого расширенного представления.
title: 'Метод Ишеллфолдервиевтипе:: Енумвиевс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.EnumViews
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e44cd774-1d16-4faa-b5ca-fcaf2740cdca
ms.openlocfilehash: 203ee36994ca3a622d564f637598f4ef22b8494200e5d57faa1d47cb290fd49b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220340"
---
# <a name="ishellfolderviewtypeenumviews-method"></a>Метод Ишеллфолдервиевтипе:: Енумвиевс

Извлекает перечислитель, возвращающий один указатель на список идентификаторов элементов (ПИДЛ) для каждого расширенного представления.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EnumViews(
  [in]  ULONG       grfFlags,
  [out] IEnumIDList **ppenum
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*грффлагс* \[ окне\]
</dt> <dd>

Тип: **ulong**

Флаги, указывающие, какие элементы следует включить в перечисление. Список возможных значений см. в разделе перечислимый тип [**шконтф**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) . Этот параметр можно игнорировать.

</dd> <dt>

*ппенум* \[ заполняет\]
</dt> <dd>

Тип: **[ **иенумидлист**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***

Адрес переменной-указателя типа [**иенумидлист**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) , которая получает перечислитель.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Представления представлены пользователю в виде скрытых папок из корневого каталога (представленного PIDL). При необходимости представление по умолчанию (в корневой папке) представляется как null или пустое **значение** Пидл.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




