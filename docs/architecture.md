\# Basic system architecture



\## High-level overview



```text

Source systems  -- Systems that generate or provide the data for the company

&#x20;     |

&#x20;     |

&#x20;     V

Landing Layer  -- Raw data storage layer, keeps data as is from source systems

&#x20;     |

&#x20;     |

&#x20;     V

Staging layer  -- Performs initial cleaning of the landing data which is cleansing, standardization, and validation

&#x20;     |

&#x20;     |

&#x20;     V

Data Warehouse -- stores integrated, historical and analytically modeled data

&#x20;     |

&#x20;     |

&#x20;     V

Data Marts     -- provides data for downstream users for analytical purpose

&#x20;     |

&#x20;     |

&#x20;     V

BI / Analytics  -- reports, visualization, ai-ml predictions





