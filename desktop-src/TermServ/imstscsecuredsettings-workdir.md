---
title: Имстсксекуредсеттингс WorkDir, свойство
description: Указывает рабочий каталог запускаемой программы.
ms.assetid: e67f7274-be47-42c4-9267-a05bb93e6725
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства WorkDir
- Службы удаленных рабочих столов свойства WorkDir, интерфейс Имстсксекуредсеттингс
- Службы удаленных рабочих столов интерфейса Имстсксекуредсеттингс, свойство WorkDir
- Службы удаленных рабочих столов свойства WorkDir, интерфейс Имсрдпклиентсекуредсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентсекуредсеттингс, свойство WorkDir
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.WorkDir
- IMsTscSecuredSettings.get_WorkDir
- IMsTscSecuredSettings.put_WorkDir
- IMsRdpClientSecuredSettings.WorkDir
- IMsRdpClientSecuredSettings.get_WorkDir
- IMsRdpClientSecuredSettings.put_WorkDir
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cc6bd8ffe1e2d2f5b835090ee1dec5e3420a8bfb2d5801b3f5f903b3436bf66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118853146"
---
# <a name="imstscsecuredsettingsworkdir-property"></a>Свойство Имстсксекуредсеттингс:: WorkDir

Указывает рабочий каталог запускаемой программы.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_WorkDir(
  [in]  BSTR newVal
);

HRESULT get_WorkDir(
  [out] BSTR *pWorkDir
);
```



## <a name="property-value"></a>Значение свойства

Новый рабочий каталог. Максимальная длина этой строки равна максимальному **\_ пути**-1 символам.

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="remarks"></a>Remarks

Дополнительные сведения см. в руководстве [по обеспечению безопасности клиента RDP](providing-for-rdp-client-security.md) .

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ имстсксекуредсеттингс определен как c9d65442-a0f9-45b2-8f73-d61d2db8cbb6<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**имсрдпклиентсекуредсеттингс**](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[**имстсксекуредсеттингс**](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





